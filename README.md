# vcal2text - display Outlook meeting requests in mutt

Meeting requests sent from Outlook/Exchange are often missed due to
being "hidden" behind a higher-priority text part. This script and
mutt configuration ensures they're displayed in a nice format.

The original source was http://dollyfish.net.nz/ but that site appears
to be gone.

Dave Holland <dave@biff.org.uk>

## Installation:

1. copy `vcal2text` to somewhere suitable, e.g. `~/bin` (make sure
   it's executable: `chmod 755 vcal2text`)
2. add these lines to your ~/.muttrc file:
```
alternative_order text/calendar text/enriched text/plain text
auto_view text/calendar
```
3. add this line to your ~/.mailcap file:
```
text/calendar; ~/bin/vcal2text '%s'; copiousoutput
```
4. install the necessary Perl libraries:
```
sudo apt-get install libdata-ical-perl libtext-autoformat-perl
```
5. enjoy your meeting requests :)

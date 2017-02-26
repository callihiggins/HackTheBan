### Goal
The goal here was to create a simple interface to edit documents and create html. We settle on google docs and google drive.

This started as an attempt to update [this pdf](https://ccrjustice.org/sites/default/files/assets/files/CCR_If_An_Agent_Knocks.pdf
), to extract the content and create a nice html page for it.

Largely inspired by this [gist](https://gist.github.com/dsager/fc11ba67574947cbc3c9), and could use this [library](https://github.com/Devex/gdocparse).

### Extracting Text from a PDF

Using this [pdf](https://ccrjustice.org/sites/default/files/assets/files/CCR_If_An_Agent_Knocks.pdf
) and this [tool](http://www.foolabs.com/xpdf/home.html).

```
pdftotext  -raw  CCR_If_An_Agent_Knocks.pdf  output.txt
```

Some useful regex's used to clean it up:

* regex `-\n` to to fix hyphenation
* `^\d*$` to remove lines that are only numbers
* `If An Agent Knocks - .*$` to remove subtitles

Also useful: https://regex101.com/

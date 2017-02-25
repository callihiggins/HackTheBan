

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

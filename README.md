# quafira

A personalised Quarto HTML document template using [Fira Sans](https://github.com/bBoxType/FiraSans/) and with nice support (to come!) for gt tables and ggplot2 charts.

** IN DEVELOPMENT **

## To use

In your project directory where you want to create Quarto reports, just type at the terminal prompt:

```
quarto add francisbarton/quafira
```


### Working notes

I've used a data-uri strategy for embedding the fonts inspired by [firasans.kit](https://github.com/dnordstrom/firasans.kit) by dnordstrom.

firasans.kit is 11 years old and I've found a more recent (in fact the latest) version (v4.3) of Fira Sans in WOFF2 format on GitHub.
I've also used the "compressed" version of the files to reduce size, at the cost of potentially reducing the quality of the font render.
For my purposes I doubt this will matter.
Using the more recent version also may not make any noticeable difference but it makes sense to use it.
And it is the last version of Fira Sans so it is stable by default.

I did consider using [FiraGO](https://github.com/bBoxType/FiraGO) (the successor to Fira Sans, with broader internationalisation support (it supports Arabic, Georgian and other scripts)), but I suspect the file size would be larger as there are more character sets supported that I am unlikely to ever make use of, realistically.


I have used [woff2base](https://hellogreg.github.io/woff2base/) to convert the current Fira web font to a base64 uri string.

I think [bookup-html](https://github.com/juba/bookup-html) by juba is quite close to what I want to achieve.

I'm hoping to build in some good CSS defaults that will apply to [{gt}](https://gt.rstudio.com/) tables even when toggling between light and dark modes.

I want to write a custom R function that will generate and open up a quarto template using this custom format when I run it.
I'm tired of copying and pasting YAML and other setup boilerplate from qmd file to qmd file.

## NEWS

### 30 May 2024

Changing back from Fira GO to Fira Sans Compressed indeed reduces `embed_fonts.scss` from 1.31MB to 865KB, nearly a 50% reduction.
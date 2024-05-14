# quafira

A personalised Quarto HTML document template using ~~Fira Sans~~ [Fira GO](https://bboxtype.com/typefaces/FiraGO/) and with nice support for gt tables and ggplot2 charts.

** IN DEVELOPMENT **

## To use

In your project directory where you want to create Quarto reports, just type at the terminal prompt:

```
quarto use template francisbarton/quafira
```


### Working notes

I'm planning to use [firasans.kit](https://github.com/dnordstrom/firasans.kit) by dnordstrom.

firasans.kit is 11 years old and I'm wondering if it is better - if it even makes any difference - to use more recent versions of Fira.

I found [woff2base](https://hellogreg.github.io/woff2base/) and will try to use that for converting the current Fira web font to a base64 uri string.

[FiraGO](https://github.com/bBoxType/FiraGO) is Fira Sans but with broader internationalisation support (supports Arabic, Georgian and other scripts).

I think [bookup-html](https://github.com/juba/bookup-html) by juba is quite close to what I want to achieve.

I'm hoping to build in some good CSS defaults that will apply to [{gt}](https://gt.rstudio.com/) tables even when toggling between light and dark modes.

I want to write a custom R function that will generate and open up a quarto template using this custom format when I run it.
I'm tired of copying and pasting YAML and other setup boilerplate from qmd file to qmd file.


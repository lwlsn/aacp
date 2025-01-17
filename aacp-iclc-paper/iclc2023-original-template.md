---
# This template is licensed under a Creative Commons 0 1.0 Universal License (CC0 1.0). Public Domain Dedication.

title: Title goes here
author:
  - name: Author one
    affiliation: University of Live Coding
    email: one@livecode.mx
  - name: Author two
    affiliation: University of Bricolage Programming
    email: two@onthefly.ca
  - name: Author three
    affiliation: University of Creative Coding
    email: three@creative.uk
abstract: |
  Replace this text with a maximum 300 word abstract. You'll find it in the
  'metadata block' at the top of your markdown document), be sure that
  each line of the abstract is indented.
fontsize: 11pt
geometry: margin=2cm
fontfamily: libertine
fontfamily: inconsolata
mainfont: Linux Libertine O
monofont: Inconsolata
bibliography: references.bib
...

# Introduction

Welcome to the markdown (aka commonmark) template for the
International Conference on Live Coding 2023.

This document is a guide to using markdown for the conference, and is
itself written in markdown. For full understanding, refer to
iclc2023.txt to see the source of this document, and iclc2023.pdf to
see the typeset output. Use of this template is currently only
recommended for those familiar with commandline tools.

We suggest you take a copy of this template (iclc2023.txt), and use it
as a starting point for your ICLC paper.

Preparing your submission using markdown will enable us to make proceedings
available both in PDF files suitable for print, and in HTML suitable
for the web. This is useful for making sure your paper is fully
accessible, via Internet search, and with assistive technology such as
screen readers for blind people. We recommend taking a straightforward approach to
formatting your document.

If you do not wish to use markdown, please do not be discouraged from
submitting your paper. There is also a word document template
available from the conference website.

# Learning and using markdown

We are happy to answer any questions you have about markdown in connection with your
conference submission.

If you have questions, you can email us directly:
  [iclc@creativecodingutrecht.nl](mailto:iclc@creativecodingutrecht.nl)

## Running pandoc {#pandoc}

Pandoc is software which turns text written in markdown into a
beautiful looking document, complete with references. You will need to
run it to create PDF documents of your paper for checking and
uploading for peer review.

You may download pandoc for all major operating systems (including MS
Windows, Apple Mac OS and GNU/Linux) from the following website:
[http://pandoc.org](http://pandoc.org)

As an alternative to the above downloads, on OS X only, the homebrew
package manager can be used to install pandoc: [http://brew.sh/](http://brew.sh/)

If you use homebrew to install on OS X you will need to install the pandoc package as follows:
```
brew update
brew install pandoc
```

To produce PDF files you will need to have LaTeX installed, as well as
pandoc. See the pandoc website for installation instructions:
[http://pandoc.org/installing.html](http://pandoc.org/installing.html). LaTeX
is used internally, you will not have to edit any LaTeX documents.

To render your markdown source as HTML, open a terminal window, change
into the folder where the template is and run the following command:

~~~~ {.bash}
pandoc --template=pandoc/iclc.html --citeproc --number-sections iclc2023.md -o iclc2023.html
~~~~

To produce a PDF document, make sure you have LaTeX installed (see
above), and run the following:

~~~~ {.bash}
pandoc --template=pandoc/iclc.latex --citeproc --number-sections iclc2023.md -o iclc2023.pdf
~~~~

For a higher quality output, add the option `--latex-engine=xelatex`
to the above. You will need the [Inconsolata](http://levien.com/type/myfonts/inconsolata.html) and [Linux Libertine](http://www.linuxlibertine.org/index.php?id=91&L=1) opentype fonts installed.

An example Makefile is also provided to run these commands for you. If you have *make* installed, you can use it to build the pdf files.

## Bibliographic references

Pandoc accepts bibliographic databases in a range of formats, so make
sure you have the right extension on your file.

  Format            File extension
  ------------      --------------
  MODS              .mods
  BibLaTeX          .bib
  BibTeX            .bibtex
  RIS               .ris
  EndNote           .enl
  EndNote XML       .xml
  ISI               .wos
  MEDLINE           .medline
  Copac             .copac
  JSON citeproc     .json

Table: Supported bibliography formats with file extension.

Authors may be referenced in two ways; inline, e.g. @Schwitters32
wrote the Ursonate sound poem, or in parenthesis, e.g. Ursonate is a
sound poem [@Schwitters32]. Multiple references should be grouped
together like so [@Schwitters32;@Miller56;@Greenewalt46].

The pandoc command given in the [above section](#pandoc) will automatically
render your references according to Chicago author-date style.

At the head of the markdown source file for this template, you will see an entry
for "bibliography" that points to the file references.bib. Here you'll find
examples of bibliography entries in BibLaTex format, including examples for
articles, books, book chapters and items from conference proceedings.

## Code

We have chosen a single column layout to better support code examples
without having to break lines. The following shows how to include a
code example with syntax highlighting:

~~~~ {.haskell}
d1 $ every 3 (iter 4) $ brak $ "bd [sn [[sn bd] sn]]*1/3"
~~~~

For more information please visit this page:
[https://hackage.haskell.org/package/skylighting]

## Figures

Images should be included as figures, with captions provided and
formatted as shown in Figure 1. Be prepared for the page layout and
image size to be changed during the editing and layout process, and
consider this when referring to the figures in the text.

![*A descriptive caption should be given for all figures, understandable without reference to the rest of the article.*](images/pomeroy.jpg)

# Conclusion

We look forward to receiving your completed papers. Submission is through the
online peer review system at https://iclc2023.creativecodingutrecht.nl/openconf.php only. 
Do not send papers directly by e-mail. In all cases, please submit a PDF version of 
your paper for peer review. At a later stage in preparing the proceedings, we may ask 
for the markdown or Word versions of your paper.

## Acknowledgments

At the end of the Conclusions, acknowledgements to people, projects, funding
agencies, etc. can be included after the second-level heading “Acknowledgments”.


# References

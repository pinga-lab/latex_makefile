# A Makefile for LaTeX Documents

Based on the adaptations by [Joshua Ryan
Smith](https://github.com/jrsmith3/latex_template) of the original work by
[Jason Hiebel](https://github.com/JasonHiebel/latex.makefile)

## Usage

You'll need to fill out some of the configuration in the `Makefile`
but setting the values of the following variables:

    # The name of the main .tex file to build.
    # Other files can be included into this one.
    PROJECT = main

    # Folder with the Latex source files
    SRC = manuscript

    # Folder where the figure files are (will assume they are EPS format)
    FIGS = figures

    # Folder where the BibTex .bib files are
    BIB = bibliography

    # Folder where the .cls .bst and .sty style files are
    STYLES = $(SRC)

These are the primary targets defined:

* `all`: Compiles the document and converts the result to a PDF file.
* `display`: Displays the compiled document in a standard PDF viewer. Linux
  uses Evince and Mac OSX uses the system specified default (likely Preview).
* `clean`: Clean up the build. Removes the output folder and EPS-to-PDF
  converted figures.
* `wc`: Approximate word count in the generated PDF.

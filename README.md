## Introduction


[![License](https://img.shields.io/badge/license-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0.html)


Documentation and bookdown for dsSynthetic package to generate synthetic data in DataSHIELD.

https://tombisho.github.io/synthetic_bookdown/


dsSynthetic has a server-side component

https://github.com/tombisho/dsSynthetic

and a client side package

https://github.com/tombisho/dsSyntheticClient


## Bookdown

The complete bookdown, tutorial, vignette with executable code and synthetic data is available here:

https://tombisho.github.io/synthetic_bookdown/



## Quick start

Please install R and R Studio 

   https://www.rstudio.com/products/rstudio/download/preview/


Install the following packages:


```r

install.packages('devtools')
library(devtools)
devtools::install_github('tombisho/dsSyntheticClient')
devtools::install_github('datashield/dsBaseClient@6.1.1')
install.packages('rmarkdown')
install.packages('knitr')
install.packages('tinytex')
install.packages('metafor')
install.packages('DSOpal')
install.packages('DSI')
install.packages('opalr')

```


## Usage

See the bookdown below for a complete tutorial:


https://tombisho.github.io/synthetic_bookdown/



A minimal example of a book based on R Markdown and **bookdown** (https://github.com/rstudio/bookdown). 

The bookdown can be compiled by typing the following commands:

  ```r 
  
  library(bookdown)

  bookdown::serve_book()
  
  ```


## Contact

Tom R.P. Bishop and Soumya Banerjee

sb2333@cam.ac.uk


## Recipe for creating your own bookdown

Bookdown recipe:

1.       In RStudio, install the bookdown package

2.       Start a new project, but choose the project to be a book.

3.       In Github create an empty project  (no README.md) with the same name as your book

4.       In RStudio go to Tools -> Project options -> Version control -> Git (it will ask you to reload the project)

5.  On Git command line, add the remote and push:
 git remote add origin https://github.com/USERNAME/PROJECT.git
git push -u origin master

6.       In the file _bookdown.yml, and the line output_dir: "docs"

7.       In the file _output.yml, delete the parts that refer to generating a pdf (I couldn’t get this to work):
 bookdown::pdf_book:
includes:
	in_header: preamble.tex
	latex_engine: xelatex
	citation_package: natbib
keep_tex: yes
bookdown::epub_book: default

8.       Start to write your book!

9.       Check in local changes

10.   In Github go to Settings -> Pages and set the source to the main branch and folder to docs

11.   Push your local changes to Github, hopefully it will build your site

This is a minimal example of a book based on R Markdown and **bookdown** (https://github.com/rstudio/bookdown). Please see the page "Get Started" at https://bookdown.org/home/about/ for how to compile this example.

Recipe by Tom Bishop

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

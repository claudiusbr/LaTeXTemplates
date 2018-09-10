# LaTeXTemplates
Some templates for LaTeX, CSS and other styling/markup which I use more regularly.

## How to use

This will depend on how you normally configure your markup. Below are a ways
which I am currently doing for each. I'm sure there are better ways to do it, I
just haven't had the time to research them.

### The HTML and CSS

I am using these mainly with converted Markdown files. The steps normally
involve, roughly:

- copy the [basicStyleSheet.css](./basicStyleSheet.css) to the folder where the
  final html file will be. e.g.:

    $ cp basicStyleSheet.css $HOME/newProject/

- copy the contents of the [basicHTMLHeaders.html](./basicHTMLHeaders.html) to
  the empty HTML file which I want to compile from markdown. E.g.:

    $ cp basicHTMLHeaders.html $HOME/newProject/my-html-file.html
  
- convert the markdown file to html, and append it to the file created above.
  E.g. (using [Pandoc](http://pandoc.org/index.html)):

    $ pandoc contents.md --from markdown --to html >> $HOME/newProject/my-html-file.html

- append the tail [basicHTMLTail.html](./basicHTMLTail.html). E.g:

    $ cat basicHTMLTail.html $HOME/newProject/my-html-file.html

### The LaTeX templates

I normally just do it all manually at the moment, so use the template as the
document header, type in the content, then use something like _pdflatex_ to
convert to pdf. But now I'm gonna start using
[Pandoc](http://pandoc.org/index.html) here too when I can.

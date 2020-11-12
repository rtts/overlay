Overlay
=======

***Quickly apply an overlay to every page of a PDF file***

Overlay is a simple bash script that overlays one PDF file over
another. It takes the first page of the _first_ PDF file, and overlays
it onto _every_ page of the second PDF file. In the typical use case,
the first PDF would contain a header/footer/stamp/watermark and the
second PDF file contains multiple pages of content. `overlay` will
combine these two PDF files into a single one so that now every page
contains the header/footer/stamp/watermark.

Installation
------------

Overlay uses [LaTeX](https://www.latex-project.org/) to produce the
final PDF file. On Debian-based distributions the following command
will install the required packages:

    apt install textlive-latex-extra

On MacOSX, use the following command:

    brew install mactex

On Windows, use
[WSL](https://docs.microsoft.com/en-us/windows/wsl/install-win10) so
you can use the `apt` command above :-)

Usage
-----

    ./overlay <first-PDF-file> <second-PDF-file> [<output-PDF-file>]


Contributing
------------

I created `overlay` because I could not find any other way of merging
two PDF files by overlaying them. However, the use of LaTeX for this
relatively simple operation is somewhat overkill.

Do you know of another solution to overlay two PDF files? Or do you
perhaps have some pointers to help me implement `overlay` without the
LaTeX dependency? If so, I would love to hear from you!

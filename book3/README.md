Python for Everybody
--------------------

These \*.mkd files are now the master files for the book (i.e. 
I will not run the conversion any more).

To produce the PDF of the book, you will need to install LaTeX on your 
system.  For Debian-derived (Ubuntu, Mint, etc.) Linux:

    sudo apt-get install texlive-full
    sudo apt-get install pandoc

For Macintosh,

    https://www.tug.org/mactex/
    https://www.tug.org/mactex/mactextras.html

To produce the book run

    bash book.sh

The output `bash book.sh` is in the file `x.pdf` and `x.epub`.

*Note that the build scripts require Python 2*

## Alternate Build Scripts

In addition to the official `book.sh1`, there are other build scripts that make
alternate versions of the book.

* `htmlbook.sh` will make an html verion of the book, with interactive examples
embedded in trinkets. These files are in `books/html` if you want to download
or view them.
* `zipbook.sh` will make two html versions of the book with Trinket branding,
one with interactive examples (that require an internet connection to work) and one with 
syntax highlighted code blocks for completely offline viewing.  A zip containing 
these is at `/book/zips/pfe.zip` if you'd just like to download it.
* `trinketbook.sh` will make the nunjucks template that we use to host the book
at [books.trinket.io](https://books.trinket.io).  This is likely not of use to you
unless you're looking for an example of how to get the book source into your own
templating language.  If you'd like to see the output of this script it's in
`books/trinket/pfe`.

If you'd like to make your own build script, you can use these as examples. If
your build script might have use to others, consider contributing it in a pull request.
Note that each build script plays nicely with the others and the represent parallel
workflows.  Please don't alter any of the python scripts that are used by another
script if you intend on contributing a new script. 

## KindleGen

The `book.sh` script will generate the `x.mobi` file is KindleGen is in the path:

    https://www.amazon.com/gp/feature.html?docId=1000765211

For Linux:

    curl -O http://kindlegen.s3.amazonaws.com/kindlegen_linux_2.6_i386_v2_9.tar.gz
    tar xfv kindlegen_linux_2.6_i386_v2_9.tar.gz 
    cp kindlegen /usr/local/bin

## Contributing

If you want to contribute, feel free to fork the pythonlearn
repository and send me pull requests.   

https://github.com/csev/py4e

We can also use the issue tracker to coordinate if that helps.

/Chuck


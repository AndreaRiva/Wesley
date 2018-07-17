Wesley

Recursively searches a directory path for image files (JPEG, GIF, PNG) and
applies lossless compression to files in-place.  This can be particularly
handy for optimizing images in an existing codebase, especially when you are
geared for working from the Linux or Mac command-line.

This script uses techniques described in this article about the use
of jpegtran: http://www.phpied.com/installing-jpegtran-mac-unix-linux/
and used by the smush.it tool described here:
http://developer.yahoo.com/yslow/smushit/faq.html

Wesley makes use of gifsicle, ImageMagick, jpegtran, and pngcrush to optimize
images. You should make an attempt to ensure that each of these has been
installed on your system prior to running this script. If you are missing
any of these, however, Wesley will still run but will skip any optimizations
for which the applicable software is not available. In other words, if you
don't have jpegtran installed, Wesley will skip JPEG optimizations.


-------------------
PACKAGES
-------------------

You're going to want to check the server you're working on to see which of
these packages you may already have, or need to install. You can still run
Wesley if you're missing one or more of these packages.  Fewer optimizations
will be made, however.

jpegtran
http://sylvana.net/jpegcrop/jpegtran/

gifsicle
http://www.lcdf.org/gifsicle/

pngcrush
http://pmt.sourceforge.net/pngcrush/

ImageMagick
http://www.imagemagick.org/

-------------------
INSTALLATION
-------------------

MAC:

1. Open the terminal

2. Install [Homebrew](https://brew.sh/) if you don't have it already

3. Install dependencies with this command ` sh install-on-mac.sh `

LINUX:

1. Open the terminal

2. Install dependencies with this command ` sudo sh install-on-linux.sh `

-------------------
USAGE
-------------------

Recursively optimize all images within a directory:

  wesley.pl directory_path

Optimize a single image:

  wesley.pl filename


-------------------
MORE INFO
-------------------

Original author: Mike Brittain

Homepage: http://www.mikebrittain.com/blog/wesley/

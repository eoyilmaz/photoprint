PhotoPrint 0.4.2 - a utility to print multiple images per sheet, using
Gutenprint, with support for 16-bit images and ICC profiles.

*WARNING* This software is experimental - use it at your own risk.

Currently JPG, BMP, TIFF and PNM images are supported natively, and other formats
are supported through the use of GdkPixbuf.  If you come across any file
that PhotoPrint won't handle, please contact me at blackfive@fakenhamweb.co.uk,
with a copy of the offending image, and I'll do my best to fix the problem.


Requirements:
~~~~~~~~~~~~~

To compile and run PhotoPrint you will need:

    * Gutenprint 5.0.0 or later
    * LittleCMS
    * GTK+ 2.4 or later
    * NetPBM
    * LibJPEG
    * LibTIFF
    * CUPS (optional)

(For compiling, of course, you need GCC and all the appropriate -devel packages installed.)

Compile Under Fedora/RHEL/CentOS
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

To compile under Fedora/RHEL/CentOS:

    sudo dnf install gutenprint-devel gutenprint-libs gutenprint-extras gutenprint-libs-ui gutenprint-cups lcms-devel
    export LIBS=X11
    ./configure
    make


Usage:
~~~~~~

photoprint [options] [image1] ...

options are:
-p - use alternative preset file
-b - batch mode

Create a folder in your home directory to store photoprint's preset files,
called .photoprint

Use the printer setup menu options to create settings suitable for your
printer, and select Save Preset, Save As or Save Default to store them to disk.

The user interface should be reasonably self-explanatory.

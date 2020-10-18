odtphp
======

### Original description

OdtPHP is a library to quickly generate Open Document Text-files that can be read by a [gigantic set][3] of Office Suites, including LibreOffice, OpenOffice and even Microsoft Office from PHP code. It uses a simple templating mechanism.
See the tests/ folder for a set of examples.

This repository already includes the changes suggested by [Vikas Mahajan][1] and a number of other bug fixes.

### History

This project was initially started by Julien Pauli, Olivier Booklage, Vincent Brouté and published at [http://www.odtphp.com][2] (link leads to archived version of page, as it is not available any longer).

### History II

This fork was done due to the fact, that the contained pclzip.lib.php and the contained PclZipProxy.php try to create a tmp-folder within the source code directory. Using suexec or php-fpm under a user without writing-permissions to the source-dir caused permission-problems.

To solve this, the 
const TMP_DIR
in PclZipProxy.php
and
define( 'PCLZIP_TEMPORARY_DIR', '' );
in pclzip.lib.php had to be edited.


### Links:

* http://sourceforge.net/projects/odtphp/ Sourceforge Project of the initial library (stale)

[1]: http://vikasmahajan.wordpress.com/2010/12/09/odtphp-bug-solved/
[2]: https://web.archive.org/web/20120531095719/http://www.odtphp.com/index.php?i=home
[3]: https://en.wikipedia.org/wiki/OpenDocument_software#Text_documents_.28.odt.29

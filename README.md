# A client-side ANT build script


## What it does

- Creates a new distribution with all needed files and optimized CSS, JavaScript, HTML and images
- Combines and minifies CSS files
- Combines, cleans and minifies JavaScript files
- Optimizes JPGs and PNGs (Unix only)


## Requirements

- [Java 1.6](http://www.oracle.com/technetwork/java/javase/downloads/index.html)
- [Apache ANT](http://ant.apache.org/bindownload.cgi]) v1.8.2+
- [JPEGTRAN](http://www.phpied.com/installing-jpegtran-mac-unix-linux/) for Mac/Unix


## Setup: Mac

- Download the latest version of [Apache ANT](http://ant.apache.org/bindownload.cgi]) and move it to `/Applications/`
- If necessary download the latest version of [YUI Compressor](http://yuilibrary.com/download/#yuicompressor) and [PNGtastic](http://code.google.com/p/pngtastic/downloads/list) and move it to `/build/tools`

- If you haven't already done it, install Homebrew:

```
ruby -e "$(curl -fsSkL raw.github.com/mxcl/homebrew/go)"
```
- Install [Libjpeg](http://arcoleo.org/dsawiki/Wiki.jsp?page=How%20to%20Install%20Libjpeg%20on%20Mac) (we only use [JPEGTRAN](http://www.phpied.com/installing-jpegtran-mac-unix-linux/)):

```
brew install libjpeg
```


## Setup: Windows

- [Download](http://ant.apache.org/manual/install.html) and [install](http://www.nczonline.net/blog/2012/04/12/how-to-install-apache-ant-on-windows/) the latest version of [Apache ANT](http://ant.apache.org/manual/install.html)


## Using the Build Script

Open terminal app or command line and go to:

```
cd ~/Sites/your-site/build/
```

### Build targets

```
ant deploy  		# Create a new distribution with optimized CSS, JavaScript, HTML and images

ant deploy.css		# Combine and minify CSS files
ant deploy.js		# Combine, clean and minify JavaSscript files
ant deploy.png		# Optimize PNGs
ant deploy.jpg		# Optimize JPGs

ant archive			# Creates a backup of your development directory w/o svn, git, deployed versions
ant backup			# Creates a full backup of your development directory
ant clean			# Remove all logs, docs, deployed versions

ant help			# Show all possible targets
```


## License
Dual licensed under the MIT and GPL licenses.

- MIT - [http://www.opensource.org/licenses/mit-license.php](http://www.opensource.org/licenses/mit-license.php)
- GNU - [http://www.gnu.org/licenses/gpl-3.0.html](http://www.gnu.org/licenses/gpl-3.0.html)


Copyright © 2013 Falko Behr, [falkonien.de](http://falkonien.de)
# A client-side ANT build script

## What it does

- Combine and minify CSS files
- Combine and minify JavaScript files
- Optimize JPGs and PNGs

## Requirements

- [Java 1.6](http://www.oracle.com/technetwork/java/javase/downloads/index.html)
- [Apache ANT](http://ant.apache.org/bindownload.cgi])
- [YUI Compressor](http://yuilibrary.com/download/#yuicompressor)
- [JPEGTRAN](http://www.phpied.com/installing-jpegtran-mac-unix-linux/)
- [PNGtastic](http://code.google.com/p/pngtastic/downloads/list)

## Setup the build tools for Mac

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

## Using the Build Script

Open terminal app or command line and go to:

```
cd sites/your-site/build/
```

### Build targets

```
ant deploy  		# Optimize CSS, JS and images
ant deploy.css		# Combine and minify CSS files
ant deploy.js		# Combine and minify JS files
ant deploy.img		# optimize JPGs and PNGs
```
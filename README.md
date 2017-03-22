# CSS Orientation Test

*CSS Half-Width Orientation Test* and *CSS Full-Width Orientation Test* are special-purpose OpenType fonts that are based on the Adobe-Identity-0 ROS (*ROS* stands for /Registry, /Ordering, and /Supplement, and refers to the /CIDSystemInfo dictionary entries that define the glyph set name for CID-based character collections). The Adobe-Identity-0 ROS is a special-purpose character collection whose use is not tied to a specific language, and these are *special-purpose* OpenType fonts that are intended to render all Unicode code points using glyphs that indicate the glyph orientation based on the writing direction, thus the reason why the Adobe-Identity-0 ROS was chosen as the basis for this OpenType font.

##  Features

These fonts include 2,050 glyphs (CIDs 0 through 2049), and map 1,111,998 Unicode code points to their 2,048 horizontal glyphs. CIDs 1 through 2048 are the horizontal glyphs, and are all the same. 2,048 glyphs are used for a more efficient (smaller) 'cmap' table size. CID+2049 is a single vertical glyph. The 2,048 High and Low Surrogates (U+D800 through U+DFFF), the two noncharacters in the BMP and in each of the 16 Supplementary Planes (FFFE and FFFF), and the 32 noncharacters in the range U+FDD0 through U+FDEF are explicitly and intentionally excluded. The 2,048 horizontal glyphs in each font map to a single vertical glyph via the '[vert](http://www.microsoft.com/typography/otspec/features_uz.htm#vert)' (Vertical Alternates) GSUB feature. As fully-functional OpenType fonts, the following 14 'sfnt' tables are included: CFF, DSIG, GSUB, OS/2, VORG, cmap, head, hhea, hmtx, maxp, name, post, vhea, and vmtx.

The images below show the functional glyphs in *CSS Half-Width Orientation Test* and *CSS Full-Width Orientation Test* (CID+1, the first of the 2,048 horizontal glyphs, and CID+2049, the single vertical glyph, are shown):

![alt text](https://raw.githubusercontent.com/adobe-fonts/css-orientation-test/master/images/half-width-hv-320.jpg "half-width") ![alt text](https://raw.githubusercontent.com/adobe-fonts/css-orientation-test/master/images/full-width-hv-320.jpg "full-width")

Note that within each OpenType font the vertical advance of the vertical glyph is one-half that of the horizontal advance of the horizontal glyphs, whose purpose is so that testing-automation scripts can more easily detect the glyph orientation and thus whether the 'vert' GSUB was applied correctly by measuring the metrics of the rendered text.

## Font installation instructions

* [OS X](http://support.apple.com/kb/HT2509)
* [Windows](http://windows.microsoft.com/en-us/windows-vista/install-or-uninstall-fonts)
* [Linux/Unix-based systems](https://github.com/adobe-fonts/source-code-pro/issues/17#issuecomment-8967116)

## Building the fonts from source

### Requirements

To build the binary font files from source, you need to have installed the [Adobe Font Development Kit for OpenType](http://www.adobe.com/devnet/opentype/afdko.html) (AFDKO). The AFDKO tools are widely used for font development today, and are part of most font editor applications.

### Building the font

In this repository, all necessary files are in place for building the OpenType/CFF fonts, and the COMMANDS.txt file provides the command lines that are used.

## Getting Involved

Send suggestions for changes to the CSS Orientation Test project maintainer, [Dr. Ken Lunde](mailto:lunde@adobe.com?subject=[GitHub]%20CSS%20Orientation%20Test), for consideration.

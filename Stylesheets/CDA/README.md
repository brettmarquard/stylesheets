# CDA Stylesheet
## Introduction
This folder contains the Lantana CDA stylesheet, an open-source
renderer for CDA documents. The stylesheet transforms the XML of a CDA document
into a webpage that can be viewed in a browser or other XSLT-compatible application.

#### Some Features
-	Adapt to any device, including paper (responsive)
-	Drag and drop re-ordering of sections from the Table of Contents
-	Indicate context by highlighting current section while navigating
-	Map common header identifiers to human readable display text (mostly US)
-	Logical grouping, revamped color palette, clearer text

## Overview of Files

###Development Files
    ./cda.xsl                   The main transformation, depends on cda-style.xsl and cda-js-dependencies.xsl
    ./cda-style.xsl             Contains CSS and custom Javascript
    ./cda-js-dependencies.xsl   Contains Fixed Libraries. Referenced for offline viewing

###Distribution Files
    ./dist/cda-combined.xsl     All development files compiled into a single file. Useful for standalone offline rendering.
    ./dist/cda-combined-web.xsl All development files compiled into a single file with web references to the fixed libraries. Useful for rendering while connected to the internet.

## Installation
No installation necessary. It is recommended to use the distribution files because it's easier to work with a single standalone file vs. multiple referenced files.

## Use
Simply reference the stylesheet in the XML file and open the XML file in
Internet Explorer (Edge or older IE). To use the navigation features, select
"Allow blocked content"
```
<?xml-stylesheet type="text/xsl" href="./cda.xsl"?>
```
Alternatively use an XSLT transformation engine and open the output in your browser of
choice. The output is confirmed to work on Chrome, Internet Explorer (Edge or Older)
and Firefox.

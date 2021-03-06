# FFV1 Specification

## Introduction

This repository manages the development of specification documents for FFV1, a lossless intra-frame video codec. The goals of this specification effort are defined within the charter of the [cellar working group](https://datatracker.ietf.org/wg/cellar/charter/) of the [Internet Engineering Task Force](https://ietf.org/). Information within this repository should be considered in draft form. The most recent official version of the specification for FFV1 versions 0, 1 and 3 may be found at https://datatracker.ietf.org/doc/draft-ietf-cellar-ffv1/ and for FFV1 version 4 at https://datatracker.ietf.org/doc/draft-ietf-cellar-ffv1-v4/.

## Formatting

The FFV1 specification was initially written in lyx. In July 2015 the formatting of the specification was transitioned to Markdown to be used with xml2rfc version 2. In August 2019 the formatting was transitioned to target [xml2rfc version 3](https://tools.ietf.org/html/rfc7991).

The Markdown version of the FFV1 specification may also be converted into XML, HTML, and text formats as an IETF RFC draft based on [xml2rfc version 3](https://tools.ietf.org/html/rfc7991). Producing the RFC formats requires mmark version 2.2.8 or higher, xml2rfc version 2.32.0 or higher, xmlstarlet 1.6.1 or higher, pdfcrop v1.38 or higher, and pdf2svg 0.2.3 or higher.

Note that within ffv1.md lines that are prefixed with `SVGI:` refer to an embedded svg image as described in https://mmark.miek.nl/post/syntax/#rfc-7991-xml-output. LaTeX expressions are provided with a `SVGC:` prefix in the form of `SVGC:filename=LaTeX_formula`. Throughout ffv1.md, ASCII-art representations are provided for each LaTeX formula with `AART:` prefixes. Lines prefixed with `AART:` MUST immediately follow the line corresponding line prefixed with `SVGC:`. Lines prefixed with `SVGI:`, `SVGC:`, and `AART:` will be converted into an <artset> element in the resulting RFC XML and thus contain both the encoded SVG data as well as optionally the ASCII art fallback.

A Makefile is provided that can produce the RFC outputs.

## Version Handling

The ffv1.md file is currently intended to be used to produce documentation for both FFV1 versions 0, 1, and 3 as well as FFV1 version 4. Lines containing `{V4}` will be suppressed from the version 0,1,3 outputs while lines containing `{V3}` will be suppressed from the version 4 outputs.

## Code of Conduct

Please note that this project is developed under the [FFmpeg Code of Conduct](https://www.ffmpeg.org/developer.html#Code-of-conduct). By participating in this project you agree to abide by its terms.

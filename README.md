# Optical_Character_Recognition
# Tesseract OCR
## Table of Contents

* [Tesseract OCR](#tesseract-ocr)
  * [About](#about)
  * [Brief history](#brief-history)
  * [Installing Tesseract](#installing-tesseract)
  * [Running Tesseract](#running-tesseract)
  * [For developers](#for-developers)
  * [Support](#support)
  * [License](#license)
  * [Dependencies](#dependencies)
  * [Latest Version of README](#latest-version-of-readme)

## About

This package contains an **OCR engine** - `libtesseract` and a **command line program** - `tesseract`.

Tesseract 4 adds a new neural net (LSTM) based [OCR engine](https://en.wikipedia.org/wiki/Optical_character_recognition) which is focused on line recognition, but also still supports the legacy Tesseract OCR engine of Tesseract 3 which works by recognizing character patterns. Compatibility with Tesseract 3 is enabled by using the Legacy OCR Engine mode (--oem 0).
It also needs [traineddata](https://tesseract-ocr.github.io/tessdoc/Data-Files.html) files which support the legacy engine, for example those from the [tessdata](https://github.com/tesseract-ocr/tessdata) repository.

Stefan Weil is the current lead developer. Ray Smith was the lead developer until 2018. The maintainer is Zdenko Podobny. For a list of contributors see [AUTHORS](https://github.com/tesseract-ocr/tesseract/blob/main/AUTHORS)
and GitHub's log of [contributors](https://github.com/tesseract-ocr/tesseract/graphs/contributors).

Tesseract has **unicode (UTF-8) support**, and can **recognize [more than 100 languages](https://tesseract-ocr.github.io/tessdoc/Data-Files-in-different-versions.html)** "out of the box".

Tesseract supports **[various image formats](https://tesseract-ocr.github.io/tessdoc/InputFormats)** including PNG, JPEG and TIFF.

Tesseract supports **various output formats**: plain text, hOCR (HTML), PDF, invisible-text-only PDF, TSV and ALTO (the last one - since version 4.1.0).

You should note that in many cases, in order to get better OCR results, you'll need to **[improve the quality](https://tesseract-ocr.github.io/tessdoc/ImproveQuality.html) of the image** you are giving Tesseract.

This project **does not include a GUI application**. If you need one, please see the [3rdParty](https://tesseract-ocr.github.io/tessdoc/User-Projects-%E2%80%93-3rdParty.html) documentation.

Tesseract **can be trained to recognize other languages**.
See [Tesseract Training](https://tesseract-ocr.github.io/tessdoc/Training-Tesseract.html) for more information.

## Brief history

Tesseract was originally developed at Hewlett-Packard Laboratories Bristol UK and at Hewlett-Packard Co, Greeley Colorado USA between 1985 and 1994, with some more changes made in 1996 to port to Windows, and some C++izing in 1998. In 2005 Tesseract was open sourced by HP. From 2006 until November 2018 it was developed by Google.

Major version 5 is the current stable version and started with release
[5.0.0](https://github.com/tesseract-ocr/tesseract/releases/tag/5.0.0) on November 30, 2021. Newer minor versions and bugfix versions are available from
[GitHub](https://github.com/tesseract-ocr/tesseract/releases/).

Latest source code is available from [main branch on GitHub](https://github.com/tesseract-ocr/tesseract/tree/main).
Open issues can be found in [issue tracker](https://github.com/tesseract-ocr/tesseract/issues),
and [planning documentation](https://tesseract-ocr.github.io/tessdoc/Planning.html).

## Installing Tesseract

You can either [Install Tesseract via pre-built binary package](https://tesseract-ocr.github.io/tessdoc/Installation.html)
or [build it from source](https://tesseract-ocr.github.io/tessdoc/Compiling.html).

A C++ compiler with good C++17 support is required for building Tesseract from source.

## Running Tesseract

Basic **[command line usage](https://tesseract-ocr.github.io/tessdoc/Command-Line-Usage.html)**:

    tesseract imagename outputbase [-l lang] [--oem ocrenginemode] [--psm pagesegmode] [configfiles...]

For more information about the various command line options use `tesseract --help` or `man tesseract`.


## For developers

Developers can use `libtesseract` [C](https://github.com/tesseract-ocr/tesseract/blob/main/include/tesseract/capi.h) or
[C++](https://github.com/tesseract-ocr/tesseract/blob/main/include/tesseract/baseapi.h) API to build their own application. If you need bindings to `libtesseract` for other programming languages, please see the
[wrapper](https://tesseract-ocr.github.io/tessdoc/AddOns.html#tesseract-wrappers) section in the AddOns documentation.

Documentation of Tesseract generated from source code by doxygen can be found on [tesseract-ocr.github.io](https://tesseract-ocr.github.io/).


## License

    The code in this repository is licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.

**NOTE**: This software depends on other packages that may be licensed under different open source licenses.

Tesseract uses [Leptonica library](http://leptonica.com/) which essentially
uses a [BSD 2-clause license](http://leptonica.com/about-the-license.html).

Yale University Beamer Theme
============================

This is an unofficial LaTeX Beamer theme for individuals affiliated with Yale University, designed according to Yale's [visual identity guidelines](https://yaleidentity.yale.edu/). [Recommended proprietary fonts](https://yaleidentity.yale.edu/typefaces), including the [Yale typeface](https://yaleidentity.yale.edu/typeface/download-yale-typeface), are not included in this repository.

Installation
============

To use this theme, you need to install the Yale Beamer theme as well as the recommended fonts if you wish to use them.

## TeX Live (Linux) and MacTeX (Mac OS)

Place the contents of this folder into the following directory. In both examples, "yale" should directly contain all the files in this repository.
* TeX Live: ~/texmf/tex/latex/beamer/yale
* MacTeX: ~/Library/texmf/tex/latex/beamer/yale

See the following tutorials for more information: [installing Beamer themes in MacTeX](https://tex.stackexchange.com/questions/202312/problems-installing-custom-beamer-style-on-mac); [setting up a personal TEXMF tree](https://www.math.hmc.edu/computing/support/tex/installing/).

## MikTeX (Windows)

Please complete the following steps.
* Place all the files in this repository except for README.md and the example subdirectory directly in the following directory: C:\Program Files\<MikTeX Root>\tex\latex\beamer\base\themes
* Close all applications that use MikTeX files (editors, MikTeX utilities, etc.).
* Open the MikTeX Console.
* Open the Tasks menu and click Refresh file name database.

See [this tutorial](https://codeyarns.com/2009/11/03/how-to-install-custom-theme-for-beamer/) for more details.

## Fonts

In accordance with the [Yale guidelines](https://yaleidentity.yale.edu/typefaces), I recommend using the following fonts.
* Main Font: [YaleNew](https://yaleidentity.yale.edu/typeface/download-yale-typeface)
* Sans-Serif Font: [Mallory](https://fonts.adobe.com/fonts/mallory) or [TheSans](https://www.lucasfonts.com/fonts/thesans/) (before 2018)
These fonts can be used with XeLaTeX if you have them installed on your computer. If you are using pdfLaTeX, you can use the default Computer Modern font family.

Usage
====

To load the Yale Beamer theme, include the following in your preamble.

    \documentclass{beamer}
    \usetheme{yale}
    
The recommended fonts can be loaded with fontspec using XeLaTeX. Use the names of the fonts as they appear in your system.

    \usepackage{fontspec}
    \setmainfont[Numbers=OldStyle]{YaleNew}
    \setsansfont[
        BoldFont={TheSans B2 Bold},
        ItalicFont={TheSans B2 SemiLight Italic},
        SmallCapsFont={TheSans B4 Caps Regular}
    ]{TheSans}

Yale University Beamer Theme
============================

This is an unofficial LaTeX Beamer theme for individuals affiliated with Yale University, designed according to Yale's [visual identity guidelines](https://yaleidentity.yale.edu/). [Recommended proprietary fonts](https://yaleidentity.yale.edu/typefaces), including the [Yale typeface](https://yaleidentity.yale.edu/typeface/download-yale-typeface), are not included in this repository.

Installation
============

You need to install the Yale Beamer theme as well as any fonts you may wish to use, such as the Yale typeface.

## TeX Live (Linux) and MacTeX (Mac OS)

Place the contents of this folder into the following directory. In both examples, "yale" should directly contain all the files in this repository.
* TeX Live: ~/texmf/tex/latex/beamer/yale
* MacTeX: ~/Library/texmf/tex/latex/beamer/yale

See the following tutorials for more information: [installing Beamer themes in MacTeX](https://tex.stackexchange.com/questions/202312/problems-installing-custom-beamer-style-on-mac); [setting up a personal TEXMF tree](https://www.math.hmc.edu/computing/support/tex/installing/).

## MikTeX (Windows)

Please complete the following steps.
* Place all the files in this repository except for README.md and the example subdirectory directly in the following directory: C:\Program Files\\<MikTeX Root\>\tex\latex\beamer\base\themes
* Close all applications that use MikTeX files (editors, MikTeX utilities, etc.).
* Open the MikTeX Console.
* Open the "Tasks" menu and click "Refresh file name database."

See [this tutorial](https://codeyarns.com/2009/11/03/how-to-install-custom-theme-for-beamer/) for more details.

## Fonts

This theme is intended for use with XeLaTeX. (Please skip this section if you are using pdfLaTeX.) Simply install any fonts you would like to use onto your system. In accordance with the [Yale guidelines](https://yaleidentity.yale.edu/typefaces), I recommend using the following fonts.
* Main Font: [YaleNew](https://yaleidentity.yale.edu/typeface/download-yale-typeface)
* Sans-Serif Font: [Mallory](https://fonts.adobe.com/fonts/mallory) (after 2018) or [TheSans](https://www.lucasfonts.com/fonts/thesans/) (before 2018)

For math symbols, you can use the default Computer Modern family. For phonetic symbols, the tipa package is incompatible with XeLaTeX. Instead, you can type IPA or other unicode characters directly into your .tex source and use any font installed on your system with the appropriate characters. I recommend using [CMU Serif](https://fontlibrary.org/en/font/cmu-serif) (for consistency with math symbols set in Computer Modern), [Doulos SIL](https://software.sil.org/doulos/), or Times New Roman (if that is already installed on your system).

Usage
====

To load the Yale Beamer theme, include the following in your preamble.

    \documentclass{beamer}
    \usetheme{yale}
    
When using XeLaTeX, you can load the recommended fonts using fontspec. Use the names of the fonts as they appear on your system.

    \usepackage{fontspec}
    \setmainfont[Numbers=OldStyle]{YaleNew}
    \setsansfont{Mallory}

Most of the text in your presentation will be set using the sans-serif font. This includes Latin-letter variable names in math mode, which will look different from numbers, Greek letters, and other math symbols. For greater consistency, you may choose to typeset all math symbols using the math font. You can do this by using mathspec instead of fontspec.

    \usepackage{mathspec}
    \setmainfont[Numbers=OldStyle]{YaleNew}
    \setsansfont{Mallory}
    \setmathfont{Computer Modern}
    \usefonttheme{professionalfonts}
    
When typesetting phonetic characters, it may be helpful to define an environment in which your IPA font will be used.

    \usepackage{fontspec}
    \newfontfamily{\ipa}{CMU Serif}
    
    \begin{document}
        /{\ipa hɛˈloʊ ˈwɚld}/!
    \end{document}

    

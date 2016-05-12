# LATEX for Linux

I installed Texlive use:
```
sudo apt-get install texlive-full latex-beamer
sudo apt-get install fontforge
```
Then I install Texmaker.

All is finished,but Chinese is non-seviceable.

Use this method and use 'XeLaTeX' to Compile .tex document.

```
\documentclass{article}
  \usepackage{xeCJK}
  \setCJKmainfont{WenQuanYi Micro Hei}

  \author{jinjiachen}
  \title{learning}

\begin{document}
  \maketitle
  \tableofcontents
  \paragraph{hello world} 中文is paragraph
\end{document}
```

YES, no errors.

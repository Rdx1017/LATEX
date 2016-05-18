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

  \author{Ren Dexin}
  \title{learning}

\begin{document}
  \maketitle
  \tableofcontents
  \paragraph{hello world} 中文is paragraph
\end{document}
```

OK, no errors.

Here, I used a system font named"WenQuanYi Micro Hei",and set it as CJKmainfont.

And \usepackage{xeCJK}


But somedays ago,I want to use SimSun(宋体).

Now,I copy simsun.ttf from Windows system.

And use:

```
      sudo mkdir /usr/share/fonts/simsun
      sudo cp 存放字体的目录/simsun.ttf  /usr/share/fonts/simsun
      sudo chmod 644 /usr/share/fonts/simsun/*
      cd /usr/share/fonts/simsun
      sudo mkfontscale
      sudo mkfontdir
      sudo fc-cache -fv
```
Finish.

Try use 
> \setCJKmainfont{SimSun}


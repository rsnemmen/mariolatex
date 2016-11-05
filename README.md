Super Mario LaTeX
===================

Have you ever wanted to mark the point where you stopped writing a LaTeX document — to easily find it for resuming latex — with the help of Mario (`\mario`) or Bowser (`\bowser`)? Here is how.

![\mario](Screenshot 2016-11-04 19.28.25.png =300x)

![\bowser](Screenshot 2016-11-05 19.32.45.png =300x)

# Required latex packages

- graphicx
- wrapfigure

# Setup

1. Copy the images `Mario_Jump.png` and `NES_Bowser_5.png` to a subdirectory `figuras` in your latex document folder.
2. In the preamble of your document — after `\documentclass` and before `\begin{document}` include the following code to setup the commands `\mario` and `\bowser`:

```latex
\newcommand{\mario}{
\begin{wrapfigure}{l}{0.1\textwidth}
\vspace{-20pt}
\begin{center}
\includegraphics[width=0.1\textwidth]{figuras/Mario_Jump.png}
\end{center}
\vspace{-10pt}
\end{wrapfigure}
}
```

```latex
\newcommand{\bowser}{
\begin{wrapfigure}{l}{0.1\textwidth}
\vspace{-20pt}
\begin{center}
\reflectbox{
\includegraphics[width=0.1\textwidth]{figuras/NES_Bowser_5.png}
}
\end{center}
\vspace{-10pt}
\end{wrapfigure}
}
```

3. That’s it! Now you can use `\mario` or `\bowser`. Have fun and be productive!

# TODO

* [ ] create a latex package for CTAN

[Visit the author's web page](http://rodrigonemmen.com/) and/or follow him on twitter ([@nemmen](https://twitter.com/nemmen)).
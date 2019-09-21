## README:

Purpose:  a flexible, LaTeX based template for compiling the final PDF for
submission to NASA mission proposal calls while allowing team members
to use the writing environment they are most comfortable with.



Features:

- Best effort NASA proposal formatting
- Automatically generate:
    - table of contents with correct page numbers
    - acronym list
    - bibliography
- Overleaf friendly
- Compiling of multiple PDF files with consistent headers, footers and
  page numbering
- Allow varying page sizes and orientations (e.g. schedule fold-outs)
- Toggle supporting documents that you may not want to share with
  the full proposal team

## How to compile acronym list:

(overleaf does this automatically)
Acronym list is built on [glossaries package](https://www.ctan.org/pkg/glossaries)
after first compilation run `$ makeglossaries main.glo` from command
line and then compile again.

## External PDF example:

Example of including an external PDF that is stored in a parent
   directory (and thus not tracked by git/Overleaf) and having it show up in table
   of contents and references in LaTex:

```
\begin{landscape}
\fakesubsection{WBS}\label{sec:wbs}
\includepdf[pages=-,pagecommand={},angle=90,width=1.0\textwidth]{../WBS.pdf}
\end{landscape}
```
(depending on input PDF margins you may need to vary the width)

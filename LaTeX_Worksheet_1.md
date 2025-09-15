
# LaTeX Workshop Worksheet2

> Audience: **Beginners** progressing to **advanced** topics  
> Duration: **~2 hours**  
> Format: **Hands-on**, with mini-exercises throughout  

---

## 0) Quick Start Checklist

- ✅ Have a **TeX distribution** installed (TeX Live / MiKTeX / MacTeX) *or* an **Overleaf** account.  
- ✅ A text editor (TeXstudio, Texmaker, VS Code + LaTeX Workshop, etc.).  
- ✅ Create a new project / folder and ensure you can **compile** to PDF.
- [latex.sjtu.edu.cn](https://latex.sjtu.edu.cn/ "SJTU online latex editor")
---

## 1) What is LaTeX (and why use it)?

LaTeX is a markup language and typesetting system. You write plain text with commands describing *structure* and *formatting*, then **compile** it into professionally typeset PDFs.

**Why LaTeX?**
- **Consistency & automation**: automatic numbering, cross-references, ToC, LoF, LoT.
- **Complex documents**: sections, figures, tables, footnotes, bibliography.
- **Separation of content/style**: focus on writing; change styles later.
- **Portable plain text**: version-control friendly.
- **High-quality typography**: great defaults for kerning, hyphenation, spacing.

> **Exercise 1.1 (2–3 min)**  
> Decide: use **Overleaf** (no install) or a **local** setup (TeX Live / MiKTeX + editor). Create a blank project/file `main.tex`.

---

## 2) The Basic Document Skeleton

```latex
\documentclass[12pt]{article}
\usepackage{graphicx}   % images
\usepackage{xcolor}     % colors (used later)
\usepackage{hyperref}   % clickable refs/links (used later)

\title{My First LaTeX Document}
\author{Your Name}
\date{\today}

\begin{document}
\maketitle

Hello, LaTeX world!

\end{document}
```

**Key parts**
- `\documentclass{article}`: choose the class (`article`, `report`, `book`, `letter`, `beamer`, …).
- **Preamble** (before `\begin{document}`): load packages, define commands, set metadata.
- **Body** (between `\begin{document}` and `\end{document}`): your content.
- `\maketitle`: prints title/author/date defined in the preamble.
- Compile twice if cross-references or ToC look like `??`.

> **Exercise 2.1 (3–4 min)**  
> Paste the skeleton, replace `Your Name`, change the title, **compile** and confirm you get a PDF.

---

## 3) Paragraphs, Line Breaks, and Text Emphasis

**Paragraphs**: leave a **blank line** between paragraphs to start a new one.  
**Line break** (avoid overuse): `\\` or `\newline`.  
**Non-breaking space**: `~` (e.g., `Dr.~Smith`).  
**Comments**: `%` starts a comment to end of line.

**Inline emphasis**
```latex
\textbf{bold}, \textit{italic}, \underline{underline}, \texttt{monospace}, \textsc{Small Caps}
\emph{emphasis that toggles within italic contexts}
```

**Special characters (escape when needed)**: `# $ % ^ & _ { } ~ \`  
Example: `50\%`, `\{curly\}`, `\_underscore\_`, `\textbackslash{}`.

> **Exercise 3.1 (3 min)**  
> Write two short paragraphs. Bold a word, italicize another, and add a literal percent sign using `\%`.

---

## 4) Sectioning (Headings) and Table of Contents

Common sectioning commands in `article`:
```latex
\section{Title}
\subsection{Subtitle}
\subsubsection{Subsubtitle}
\paragraph{Run-in heading} Text...
```

**Starred versions** skip numbering: `\section*{Unnumbered}`.  
**Table of contents**: add `\tableofcontents` (after `\maketitle`); compile twice.

> **Exercise 4.1 (3–4 min)**  
> Create `\section{Introduction}` with a paragraph, then `\subsection{Motivation}`. Add `\tableofcontents` under the title and compile twice.

---

## 5) Lists: itemize, enumerate, description

```latex
\begin{itemize}
  \item Unordered list item
  \item Another point
\end{itemize}

\begin{enumerate}
  \item First
  \item Second
\end{enumerate}

\begin{description}
  \item[Term] Definition text
  \item[LaTeX] A typesetting system
\end{description}
```

Lists can be **nested** by placing one environment inside an `\item`.

> **Exercise 5.1 (3 min)**  
> Add one of each list type. Try a nested list (an `itemize` inside an `enumerate`).

---

## 6) Figures (Images)

1) Load package in preamble: `\usepackage{graphicx}`  
2) Put your image file in the project.  
3) Use a **float** with caption + label:

```latex
\begin{figure}[ht]
  \centering
  \includegraphics[width=0.65\textwidth]{example-image} % omit extension
  \caption{A helpful caption.}
  \label{fig:sample}
\end{figure}

As shown in Figure~\ref{fig:sample}, ...
```

- Placement hints: `[h]` here, `[t]` top, `[b]` bottom, `[p]` float page; combine like `[ht]`.
- Use `\centering` and set width relative to `\textwidth`.
- Reference with `Figure~\ref{...}`.

> **Exercise 6.1 (5 min)**  
> Add an image you have (PNG/JPG/PDF). Insert it with a caption and label. Reference it in text with `Figure~\ref{...}`.

---

## 7) Tables (tabular + table)

```latex
\begin{table}[h]
  \centering
  \begin{tabular}{l|c|r}
    \hline
    Item & Description & Price (USD) \\ \hline
    Widget A & Basic widget & 19.99 \\
    Widget B & Advanced widget & 29.50 \\
    Widget C & Premium widget & 45.00 \\ \hline
  \end{tabular}
  \caption{Sample widget prices}
  \label{tab:prices}
\end{table}

See Table~\ref{tab:prices} for details.
```

- `tabular` column specifiers: `l` (left), `c` (center), `r` (right), `|` vertical lines.  
- Cells separated by `&`, rows end with `\\`, lines via `\hline`.  
- Wrap in `table` for floating, caption, and labels.

> **Exercise 7.1 (6–7 min)**  
> Create a 3-column table with a header row and 3 data rows. Add caption + label. Reference it in text.

**Pro tip**: For beautiful rules, use `\usepackage{booktabs}` and replace `\hline` with `\toprule`, `\midrule`, `\bottomrule`.

---

## 8) Cross-References (labels + ref/pageref)

Attach a `\label{key}` to the thing you want to reference:
- After section: `\section{Method}\label{sec:method}`
- Inside `figure`/`table`: usually after `\caption{...}\label{...}`

Then reference it:
```latex
See Section~\ref{sec:method} on page~\pageref{sec:method}.
```

> **Exercise 8.1 (3 min)**  
> Add labels to one section, one figure, and one table. Add sentences referencing each. Compile **twice** to resolve `??`.

---

## 9) Footnotes

Inline footnotes are easy:
```latex
LaTeX was popularized by Leslie Lamport\footnote{Lamport built LaTeX on top of Knuth's TeX in the 1980s.}.
```

- Don’t leave a space before `\footnote{...}`.  
- Keep footnotes concise.

> **Exercise 9.1 (2 min)**  
> Add a footnote after a term or name in your text and compile.

---

## 10) Hyperlinks (URLs and clickable refs)

Enable in preamble:
```latex
\usepackage[hidelinks]{hyperref} % or colorlinks options
```

Add links:
```latex
\href{https://www.latex-project.org}{LaTeX Project}
\url{https://ctan.org}
```

This also makes `\ref` and `\cite` clickable.

> **Exercise 10.1 (2 min)**  
> Add a link to an external site and confirm it’s clickable in the PDF.

---

## 11) Page Layout, Fonts, and Spacing (quick tour)

**Margins/layout** (preamble):
```latex
\usepackage[a4paper,margin=1in]{geometry}
```

**Line spacing**:
```latex
\usepackage{setspace}
\doublespacing   % or \onehalfspacing
```

**Fonts** (modern approach with XeLaTeX/LuaLaTeX):
```latex
% Compile with XeLaTeX or LuaLaTeX
\usepackage{fontspec}
\setmainfont{Times New Roman} % or another installed font
```

**Headers/footers**:
```latex
\usepackage{fancyhdr}
\pagestyle{fancy}
\fancyhead{} \fancyfoot{}
\fancyhead[L]{My Title} \fancyhead[R]{\thepage}
```

> **Exercise 11.1 (5 min)**  
> Change page margins to 1in. Add a custom header with document title and page number. Re-compile.

---

## 12) Using Packages (ecosystem overview)

Load with:
```latex
\usepackage[options]{packagename}
```

Common picks:
- `graphicx` – images
- `xcolor` – colors
- `hyperref` – links & PDF metadata
- `geometry` – page layout
- `booktabs` – beautiful tables
- `fancyhdr` – headers/footers
- `enumitem` – control list spacing/labels
- `caption` – caption formatting
- `csquotes` – smart quotes
- `babel`/`polyglossia` – languages
- `minted`/`listings` – code formatting (requires shell-escape for `minted`)

> **Exercise 12.1 (2–3 min)**  
> Identify one feature you want (e.g., colored text, nicer tables, custom headers). Add the corresponding package and use one command from it.

---

## 13) Defining Your Own Commands (macros)

Avoid repetition and add semantic meaning.

**No-argument macro:**
```latex
\newcommand{\ProductName}{SuperWidget}
Our \ProductName{} is great!
```

**With arguments:**
```latex
\newcommand{\bt}[1]{\textbf{#1}} % bold text
\bt{Important}
```

**Advanced example (requires xcolor):**
```latex
\newcommand{\bluetext}[1]{\textcolor{blue}{#1}}
This is \bluetext{blue text}.
```

> **Exercise 13.1 (3–4 min)**  
> Define a `\highlight{...}` macro that uses color or `\textbf{}`. Use it twice in your text.

---

## 14) Bibliographies and Citations (overview only; optional hands‑on)

Two popular approaches:

### (A) BibTeX (classic)
1. Create `refs.bib` with entries:
   ```bibtex
   @book{knuth1984,
     author    = {Donald E. Knuth},
     title     = {The TeXbook},
     year      = {1984},
     publisher = {Addison-Wesley}
   }
   ```
2. In your `.tex`:
   ```latex
   \bibliographystyle{plain}
   \bibliography{refs} % refs.bib
   ```
3. Cite in text: `\cite{knuth1984}`. Compile sequence: LaTeX → BibTeX → LaTeX → LaTeX.

### (B) biblatex + biber (modern)
```latex
\usepackage[backend=biber,style=numeric]{biblatex}
\addbibresource{refs.bib}

% ... in body ...
According to \cite{knuth1984}, ...

\printbibliography
```

> **Exercise 14.1 (optional, 5–8 min)**  
> Create a `.bib` file with one entry, cite it once, and print the bibliography. Prefer Overleaf if you don’t want to manage the compile sequence locally.

---

## 15) Beamer Slides (bonus peek)

Create slides using the `beamer` class:
```latex
\documentclass{beamer}
\begin{document}
\begin{frame}{Title}
  Bullet points
\end{frame}
\end{document}
```

Useful when you want LaTeX-styled presentations with overlays, themes, and consistent math (if used).

---

## 16) Troubleshooting Tips

- **Common errors**: unmatched braces, missing `\end{...}`, unknown command (typo or missing package), special characters not escaped.
- **References show `??`**: compile **twice** (or enable “auto” on Overleaf).
- **Image not found**: check filename, path, and that you omitted the extension in `\includegraphics{...}` (LaTeX picks the right one).
- **Table overruns page**: consider `tabularx`, `longtable`, or reduce column width / wrapping with `p{<width>}` columns.
- **Use the community**: TeX StackExchange, CTAN, Overleaf docs.

---

## 17) Capstone: Mini-Report (10–15 min)

Create a 1–2 page mini-report that includes:
- Title/author (`\maketitle`)
- A `\tableofcontents`
- At least **two sections** and **one subsection**
- **Bold**, *italic*, and a **footnote**
- An **itemize** or **enumerate** list
- One **figure** or **table** with caption + label
- At least **two cross-references** (`\ref` + `\pageref`)

This consolidates everything you learned today.

---

## Appendix A: Starter Template (copy–paste)

```latex
\documentclass[12pt]{article}
\usepackage[utf8]{inputenc}
\usepackage{graphicx}
\usepackage{xcolor}
\usepackage[hidelinks]{hyperref}
\usepackage[a4paper,margin=1in]{geometry}
\usepackage{booktabs}
\usepackage{fancyhdr}
\pagestyle{fancy}
\fancyhead{} \fancyfoot{}
\fancyhead[L]{LaTeX Workshop} \fancyhead[R]{\thepage}

\title{LaTeX Workshop: No-Math Essentials}
\author{Your Name}
\date{\today}

\begin{document}
\maketitle
\tableofcontents

\section{Introduction}
Welcome to LaTeX! This handout covers non-math essentials for professional documents.

\section{Lists}
\subsection{Unordered}
\begin{itemize}
  \item Point A
  \item Point B
\end{itemize}

\subsection{Ordered}
\begin{enumerate}
  \item Step 1
  \item Step 2
\end{enumerate}

\section{Figures}
As shown in Figure~\ref{fig:sample}, images are first-class in \LaTeX.
\begin{figure}[h]
  \centering
  \includegraphics[width=0.6\textwidth]{example-image}
  \caption{An example image.}
  \label{fig:sample}
\end{figure}

\section{Tables}
See Table~\ref{tab:demo} for an example.
\begin{table}[h]
  \centering
  \begin{tabular}{lcr}
    \toprule
    Name & Desc & Value \\\midrule
    A & Alpha & 1.23 \\
    B & Beta  & 4.56 \\
    C & Gamma & 7.89 \\\bottomrule
  \end{tabular}
  \caption{A neat table.}
  \label{tab:demo}
\end{table}

\section{Footnotes and Links}
This is a footnote\footnote{Footnotes live at the bottom of the page.}. Visit the
\href{https://www.latex-project.org}{LaTeX Project} for more.

\end{document}
```

---

## Appendix B: Handy Reference

- **Classes**: `article`, `report`, `book`, `letter`, `beamer`
- **Headings**: `\section`, `\subsection`, `\subsubsection`, `\paragraph`
- **Text**: `\textbf`, `\textit`, `\underline`, `\texttt`, `\textsc`, `\emph`
- **Lists**: `itemize`, `enumerate`, `description`
- **Figures**: `figure` + `\includegraphics`
- **Tables**: `table` + `tabular` (or `booktabs`)
- **Cross-refs**: `\label`, `\ref`, `\pageref`
- **Footnotes**: `\footnote{...}`
- **Links**: `\href{URL}{Text}`, `\url{URL}`
- **Layout**: `geometry`, `fancyhdr`, `setspace`
- **Fonts** (XeLaTeX/LuaLaTeX): `fontspec`
- **Color**: `xcolor`
- **Code**: `listings` or `minted`

---

### End of Worksheet — Happy TeXing!

# <span style="color:#2E86C1; font-family:Georgia; font-size:32px;">📘 LaTeX Workshop Formula Part Worksheet</span>

Welcome to the <span style="color:#117A65; font-weight:bold;">LaTeX Workshop Formula Part</span> 🎉  
<span style="color:#7D3C98;">Goal:</span> Learn the basics of LaTeX math, improve clarity and consistency, and practice writing formulas using professional conventions.

---

## <span style="color:#C0392B;"> Section 1: Common Formulas (Quick Reference)</span>

Here are some **commonly used formulas** in mathematics, already written in LaTeX.  
Use them as examples and modify them in the exercises.

- **Fractions & Roots**  
  \frac{a+b}{c+d}, \quad \sqrt{x^2+y^2}
- $$
\frac{a+b}{c+d}, \quad \sqrt{x^2+y^2}
$$

- **Exponents & Logarithms**  
  e^{i\pi} + 1 = 0, \quad \log_a b = \frac{\ln b}{\ln a}
- $$
e^{i\pi} + 1 = 0, \quad \log_a b = \frac{\ln b}{\ln a}
$$

- **Limits**  
  \lim_{x \to 0} \frac{\sin x}{x} = 1, \quad \lim_{n \to \infty} \left(1 + \frac{1}{n}\right)^n = e
- $$
\lim_{x \to 0} \frac{\sin x}{x} = 1, \quad 
\lim_{n \to \infty} \left(1 + \frac{1}{n}\right)^n = e
$$

- **Derivatives**  
  \frac{d}{dx} \sin x = \cos x, \quad f'(x) = \lim_{h \to 0} \frac{f(x+h)-f(x)}{h}
- $$
\frac{d}{dx} \sin x = \cos x, \quad 
f'(x) = \lim_{h \to 0} \frac{f(x+h)-f(x)}{h}
$$

- **Integrals**  
  \int_0^1 x^2 \, dx = \frac{1}{3}, \quad \int_{-\infty}^{\infty} e^{-x^2} dx = \sqrt{\pi}
- $$
\int_0^1 x^2 \, dx = \frac{1}{3}, \quad 
\int_{-\infty}^{\infty} e^{-x^2} dx = \sqrt{\pi}
$$

- **Summations & Products**  
  \sum_{i=1}^n i = \frac{n(n+1)}{2}, \quad \prod_{k=1}^n k = n!
- $$
\sum_{i=1}^n i = \frac{n(n+1)}{2}, \quad 
\prod_{k=1}^n k = n!
$$

- **Vectors & Matrices**  
  \vec{v} = \begin{bmatrix} x \\ y \\ z \end{bmatrix}, \quad
  A = \begin{bmatrix} 1 & 0 \\ 0 & 1 \end{bmatrix}
- $$
\vec{v} = \begin{bmatrix} x \\ y \\ z \end{bmatrix}, \quad
  A = \begin{bmatrix} 1 & 0 \\ 0 & 1 \end{bmatrix}
$$
- **Set operator**
  < > \subset \supset \subseteq \supseteq
- $$
< > \quad \subset \quad \supset \quad \subseteq \quad \supseteq \quad \cup \quad \cap
$$
- **Special Symbols**  
  \alpha, \beta, \gamma, \delta, \theta, \infty, \forall, \exists, \nabla
- $$
\alpha, \beta, \gamma, \delta, \theta, \infty, \forall, \exists, \nabla
$$
### Tips
1. Check [Math expressions](https://www.overleaf.com/learn/latex/Mathematical_expressions) for more detailed information.
2. Use [Formula editor](https://www.latexlive.com/) to generate formula automatically.
---
## <span style="color:#2874A6;"> Section 2: Math Modes in LaTeX</span>

LaTeX provides **different ways** to enter math mode.  
It’s important to use the right one depending on whether you want inline or display math.

### 1. Inline Math
- **Syntax**: `\( ... \)` or single dollar `$ ... $`  
- **Use**: Inside a sentence.  
- **Example**: 
  ```latex
  This is inline math: \( a^2 + b^2 = c^2 \).  
  Or equivalently: $a^2+b^2=c^2$.
  ```

👉 In professional LaTeX (academic journals), **`\(...\)` is preferred** because `$...$` is TeX legacy and may cause spacing issues.

---

### 2. Display Math
- **Syntax**: `\[ ... \]` or double dollars `$$ ... $$`  
- **Use**: Standalone equation, centered, without numbering.  
- **Example**:  ```
  ```latex
  \[
  E = mc^2
  \]
  ```

---

### 3. Numbered Equations
- **Syntax**: `equation` environment  
- **Use**: To number a formula automatically.  
- **Example**:  
  ```latex
  \begin{equation}
  \nabla \cdot \vec{E} = \frac{\rho}{\varepsilon_0}
  \end{equation}
  ```
### 4. Multi-line Alignment
- **Syntax**: `align` (from **amsmath**)  
- **Use**: Align multi-step derivations at `=` or other operators.  
- **Example**:  

```latex
\begin{align}
f(x) &= (x+1)^2 &= ..\\
     &= x^2 + 2x + 1 &= ..
\end{align}

%or

\begin{equation}
\notag % no numbering
	\begin{aligned}
	f(x) &= (x+1)^2 \\
	     &= x^2 + 2x + 1
	\end{aligned} 
\end{equation}
```


---

## <span style="color:#CA6F1E;">Section 3: Exercises</span>

### 1. <span style="color:#2874A6;">Basic Formulas</span>
1. Write the quadratic formula:  $$
x = \frac{-b \pm \sqrt{b^2 - 4ac}}{2a}
$$

2. Write the classic limit:$$
\lim_{x \to 0} \frac{\sin x}{x} = 1
$$

👉 Use <span style="color:#AF7AC5;">`\frac`</span>, <span style="color:#AF7AC5;">`\sqrt`</span>, <span style="color:#AF7AC5;">`\lim`</span>.

---

### 2. <span style="color:#2874A6;">Alignment & Derivations</span>
1. Use the <span style="color:#D35400; font-weight:bold;">align environment</span> to typeset$$
\begin{aligned}
f(x) &= (x+1)^2 \\
     &= x^2 + 2x + 1
\end{aligned}
$$

---

### 3. <span style="color:#2874A6;">Advanced Symbols</span>
1. Integral:$$
\int_0^\infty e^{-x} \, dx = 1
$$

2. Series:$$
\sum_{n=1}^{\infty} \frac{1}{n^2} = \frac{\pi^2}{6}
$$

3. Vector:$$
\vec{v} = (x, y, z)
$$

---

### 4. <span style="color:#2874A6;">Challenge Problem</span>

$$
\lim_{n \to \infty} \int_{0}^{1} \frac{x^n}{1+x} \, dx, 
\quad
A = \begin{bmatrix}
1 & 0 & 0 \\
0 & 1 & 0 \\
0 & 0 & 1
\end{bmatrix}
$$
---

## <span style="color:#C0392B;">Section 4: Best Reminder & Tips</span>
### 1. Multi-line Alignment: `align` vs `aligned`

- **`align`**:
  - Requires `amsmath` package: `\usepackage{amsmath}`
  - Standalone multi-line equations with automatic numbering
  - Example:
```latex
\begin{align}
f(x) &= (x+1)^2 \\
     &= x^2 + 2x + 1
\end{align}
```


- Notes:
    - Use `&` to indicate alignment points (typically at `=`)
    - Use `\nonumber` or `\notag` to remove numbering on specific lines
    - Use `\label{}` for cross-references with `\eqref{}`

- **`aligned`**:
    - Also requires `amsmath`, but must be inside another math environment
    - Does not provide numbering on its own
    - Example:

```latex
\[
\begin{aligned}
f(x) &= (x+1)^2 \\
     &= x^2 + 2x + 1
\end{aligned}
\]
```

- Notes:
    - Only allowed in math environment. (Need `\begin{equation}` or `$$$$`or`\[\]`)
    - Ideal for embedding aligned equations inline or inside display math
    - For numbering, wrap in `equation` environment:

```latex
\begin{equation}
\nonumber %or \notag
\begin{aligned}
f(x) &= (x+1)^2 \\
     &= x^2 + 2x + 1
\end{aligned}
\end{equation}
```

---

### 2. Use `\mathrm{d}x` for differentials

- Differential `d` is an operator, not a variable; should be upright
    
- Example:
$$
\int_0^1 x^2 \, \mathrm{d}x
$$

```latex
\int_0^1 x^2 \, \mathrm{d}x
```

- Optional macro: $$
\newcommand{\dif}{\mathop{}\!\mathrm{d}}
\int_0^1 x^2 \,\dif x
$$
    

```latex
\newcommand{\dif}{\mathop{}\!\mathrm{d}}
\int_0^1 x^2 \,\dif x
```

---

### 3. Control spacing
 
|Command|Width|Example|
|---|---|---|
|`\,`|thin space (1/6 quad)|`a\,b`|
|`\:`|medium space (2/9 quad)|`a\:b`|
|`\;`|thick space (5/18 quad)|`a\;b`|
|`\!`|negative thin space (-1/6 quad)|`a\!b`|
|`\quad`|1 em (width of “M”)|`a \quad b`|
|`\qquad`|2 em|`a \qquad b`|
1. **Multiplication**  
   Prefer `\cdot` or thin space `\,` over implicit juxtaposition when variables are next to numbers.  
$$
2\,x \quad \text{or} \quad 2 \cdot x
$$

   ```latex
   2\,x \quad \text{or} \quad 2 \cdot x
```

2. **Function Application**  
    Always put a thin space after functions before arguments for clarity.
    $$
\sin\,x, \log\,n
$$
    
    ```latex
    \sin\,x, \log\,n
    ```
    
3. **Fractions**  
    Use small spaces around `\frac` if needed for readability.
    $$
\frac{a}{b}\,x
$$
    
    ```latex
    \frac{a}{b}\,x
    ```
    
4. **Operators in Limits/Integrals**  
    Add thin or medium space around `d` in integrals.
    $$
\int_0^1 f(x)\,\mathrm{d}x
$$
    
    ```latex
    \int_0^1 f(x)\,dx
    ```
    
5. **Negative Space**  
    Use `\!` sparingly to reduce awkward gaps in products or superscripts.
    $$
x^{n\!+1}
$$
    
    ```latex
    x^{n\!+1}
    ```

To see more detailed information in section 7 of this webpage [latex_space](https://latex-tutorial.com/latex-space/)

---

### 4. Place limits explicitly

- Inline math usually puts limits to the right; 
    $\sum_{i=1}^n i$
- Use `\limits` to force display-style limits inline:
    $\sum\limits_{i=1}^n i$

```latex
\sum\limits_{i=1}^n i
```

- Or `\displaystyle`:
    $\displaystyle \sum_{i=1}^n i$

```latex
$\displaystyle \sum_{i=1}^n i$
```

---

### 5. Use `\label` and `\ref` for numbering

- Automatic numbering and cross-references
    
- Example:
    

```latex
\begin{equation}
\label{eq:problem1_quadratic}
x = \frac{-b \pm \sqrt{b^2 - 4ac}}{2a}
\end{equation}

As shown in equation \eqref{eq:problem1_quadratic}, ...
```


- `\ref{eq:problem1_quadratic}` → prints just the number: `1`.    
- `\eqref{eq:problem1_quadratic}` → prints the number **with parentheses**: `(1)`.

---

## <span style="color:#7D6608;">Section 5: Recommended Tools</span>

- [Overleaf](https://www.overleaf.com/) — Online editor  
- [SJTULaTex](https://latex.sjtu.edu.cn/) — Online editor  
- [Obsidian](https://obsidian.md/) — Markdown + MathJax  

### 📝 Quick Obsidian Setup & LaTeX Tips

For this workshop, you will only need a **basic Obsidian setup** to write and render LaTeX formulas efficiently. We will cover this in ~5 minutes.

---

#### 1. Installing Obsidian
- Go to [https://obsidian.md](https://obsidian.md) and download the appropriate version for your OS.
- Install and open Obsidian.
- Create a new vault or open an existing one.

---

#### 2. Installing Useful Plugins
- Open **Settings → Community plugins → Browse**  
- Recommended plugins for this workshop:
  1. **Latex suite** - make typesetting LaTeX math as fast as handwriting.
  2. **Advanced Tables** – for better table editing.
  3. **Obsidian MathJax Enhancer** (optional) – adds extra math environments like `align`.

> ⚠️ Make sure to **enable community plugins** in Settings first.

---
#### 3. Quick LaTeX Shortcuts 

Here are 10 commonly used LaTeX shortcuts for fast formula writing in Obsidian:


| Trigger | Output                              | Description                    |
| ------- | ----------------------------------- | ------------------------------ |
| `dm`    | `$$$$`                              | Formula sign                   |
| `mk`    | `$$`                                | Inline formula                 |
| `@a`    | `\alpha`                            | Greek letter alpha             |
| `@b`    | `\beta`                             | Greek letter beta              |
| `sr`    | `^2`                                | Squared (superscript 2)        |
| `cb`    | `^3`                                | Cubed (superscript 3)          |
| `_`     | `_{} `                              | Subscript                      |
| `//`    | `\frac{numerator}{denominator}`     | Fraction                       |
| `ee`    | `e^{ }`                             | Exponential function           |
| `lr(`   | `\left( ... \right)`                | Automatic resizing parentheses |
| `pmat`  | `\begin{pmatrix} ... \end{pmatrix}` | Parentheses matrix             |
| `ddt`   | `\frac{d}{dt}`                      | Derivative with respect to t   |
| `beg`   | `$\begin{}\end{}$`                  | Begin command                  |

---
## Other related materials

1. [AutoTableGenerate](https://www.tablesgenerator.com/)
2. [The Comprehensive TeX Archive Network](https://www.ctan.org/)

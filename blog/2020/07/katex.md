+++
title = "KaTeX"  #  this must be given
short = raw"""
    How to use K$\alpha$Te$\chi$ with Franklin: $2\int_0^\infty {\sin(x) \over \exp(x)}\,\mathrm{d}x = 1$.
    """
published = Date(2020, 7, 14)

# specify if different than the website wide ones
post_author = "Kevin Barabash"
post_author_img = "/assets/images/kevinbarabash.jpg"
post_author_twitter = ""
post_author_insta = ""
post_author_github = "https://github.com/kevinbarabash"
+++

[KaTeX](https://katex.org/) is a simple, yet powerful, way of including maths in pages.

## Usage

Basically just use `$`, `$$`, `\begin{...}` like you would in LaTeX.

Single `$` for inline maths like so: `$i := \sqrt{-1}$` which gives: $i := \sqrt{-1}$,

Double `$$` for display maths  like so: `$$ \exp(i\pi) + 1 = 0 $$` which gives:

$$ \exp(i\pi) + 1 = 0 $$

You can also use alignment environments:

```plaintext
\begin{align}
x &= 5 \\
y &= x + 2 \\
z &= y^2 \\
\end{align}
```

which gives:

\begin{align}
x &= 5 \\
y &= x + 2 \\
z &= y^2 \\
\end{align}

or if you want more spacing, use `eqnarray`:

```plaintext
\begin{eqnarray}
x &=& 5 \\
y &=& x + 2 \\
z &=& y^2 \\
\end{eqnarray}
```

which gives:

\begin{eqnarray}
x &=& 5 \\
y &=& x + 2 \\
z &=& y^2 \\
\end{eqnarray}

if you don't want a display block to be numbered, you can wrap it in `@@no-number ... @@`

```plaintext
@@no-number
\begin{eqnarray}
x &=& 5 \\
y &=& x + 2 \\
z &=& y^2 \\
\end{eqnarray}
@@
```

which gives:

@@no-number
\begin{eqnarray}
x &=& 5 \\
y &=& x + 2 \\
z &=& y^2 \\
\end{eqnarray}
@@

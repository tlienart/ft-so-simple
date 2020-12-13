+++
title = "Basics"
short = "A short post on Franklin's syntax."
published = Date(2020, 11, 20)
+++

If you're used to writing simple markdown, then basically you won't  be surprised with Franklin.
There's a number of  useful additions (a full  list of which can be found in [the  documentation](https://franklinjl.org/syntax/markdown/)).
We show  a few examples below.

## Div blocks

You can easily specify spans  of your text which should be wrapped in a specific div blocks which can be useful for styling; use `@@divname ... @@`

@@bluebg
This part  of the text is  in a div block  for instance.
@@

You can specify multiple classes by doing `@@d1,d2,d3 ... @@`.

## Raw HTML

You can insert raw HTML putting it between `~~~` e.g.: ~~~<span style="color:red;">red span</span>~~~.

## LaTeX-style commands

On a website you might have repeating patterns (e.g. a specific block of raw HTML that you want to insert in multiple places).
Franklin  helps you define commands that help abstract away such things.
See [the docs](https://franklinjl.org/syntax/divs-commands/#latex-like_commands) for more info.

For instance  we can define a command `\css{style}{text}` which takes a block of text and add a specific style to  it:

```plaintext
\newcommand{\css}[2]{~~~<span style="#1">#2</span>~~~}
```
\newcommand{\css}[2]{~~~<span style="#1">#2</span>~~~}

and call it easily: \css{color:red}{like so}.

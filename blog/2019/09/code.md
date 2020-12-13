+++
title = "Code"
short = "Franklin supports code in more ways than one."
published = Date(2019, 7, 25)
+++

Franklin allows you to insert highlighted code with syntax highlighting provided by [highlight.js](highlightjs.org/) but, maybe more importantly, it allows you to **run** code and show the output.

## Usage

As usual in Markdown you can include code like so:

```python
import numpy as  np

r = np.log(1234)
print(np.round(r, 2))
```

Note that by default code blocks will be considered as Julia lang code blocks (unless you specify the `lang` page variable differently).
If you want to a void any highlighting, use  `plaintext`  as the language name.

## Evaluated code

With Julia code you can get the code executed directly and its output shown if you use a triple backtick followed by `!` as opening fence:

```!
r = log(1234)
print(round(r, digits=2))
```

Note that since  Julia can easily call Python or R, you could have executable python or R cells easily too (or even C or C++), see [here](https://franklinjl.org/code/eval-tricks/#python_code_blocks) for an example with python code blocks.

### Re-parsing the output

If you open with a  triple backtick followed by a name (see [the docs](https://franklinjl.org/code/#live_evaluation_julia)), you can place the output wherever you want and  can even re-parse the output as markdown:

```julia:ex
print("This is **cool** and `dandy`.")
```

the output can be inserted and re-parsed using `\textoutput`: \textoutput{ex}.
See the documentation for more information.

# JPAC Review Commands

This repository contains LaTeX commands developed to facilitate the internal review process of paper drafts.
These commands allow reviewers to leave comments, suggest corrections, and mark sections as reviewed directly within the LaTeX document.

## Main Command

### `\addReviewer{name}{color}`

This command defines a set of personalized annotation commands for a reviewer.
Replace `name` with the reviewer's identifier and `color` with a preferred color to highlight their annotations.

#### Commands Enabled by `\addReviewer`

- `\name{comment}`: Inserts a bold, colored comment into the text.
- `\namecor{original_text}{new_text}`: Strikethroughs the `original_text` and adds `new_text` in bold and color.
- `\nametodo{todo_note}`: Adds a framed note box with a TODO item.
- `\checkedby{name}`: Places a color-coded circle in the margin to indicate a section has been reviewed by the specified individuals. Use `\showCrossChecks` in your preamble to enable visual indicators.

Example:
```latex
\misha{Comment}
\mishacor{Corraboration}{Collaboration}
\mishatodo{This section should go to the earlier chapter}

\showCrossChecks % in your preamble
\begin{align}
\checkedby{misha}
t &= \frac{1}{2\pi}\int \frac{\text{Im} t(s')}{s'-s} ds'\,, 
\\ \checkedby{misha}
t &= i\text{Im}t + i\text{Re}t
\end{align}
```

## Setup

1. Include the provided style files in your LaTeX document preamble.
2. Use the `\addReviewer` command to initialize each reviewer's commands.
3. Utilize the specific commands in the LaTeX document as shown in the examples.

## Dependencies

- `mfirstuc`: For capitalizing reviewer names.
- `todonotes`: For creating todo boxes.
- `tikz, marginnote`: For creating margin notes.
- `soul, color`: Required for text styling and coloring.

Ensure these packages are included in your LaTeX setup before using the commands.

## Usage

After defining reviewers with `\addReviewer`, use the personalized commands throughout your LaTeX document to annotate and provide feedback effectively.

## Licence

Free to reuse, MIT licence.
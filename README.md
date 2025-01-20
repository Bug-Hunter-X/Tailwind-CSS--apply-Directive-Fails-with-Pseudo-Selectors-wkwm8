# Tailwind CSS @apply Directive Issue with Pseudo-Selectors

This repository demonstrates a bug where Tailwind's `@apply` directive doesn't correctly apply styles when a pseudo-selector (e.g., `&:hover`) is included in the class being applied. This results in the styles not being applied on hover, despite the class being defined correctly.

## Steps to Reproduce

1. Clone this repository.
2. Open `bug.css` to see the problematic code.
3. Open `index.html` (or a similar file, depending on your setup) in a web browser.
4. Observe that the hover effect is not applied, even though the class definition seems correct.

## Solution

The solution is to avoid using `@apply` with pseudo-selectors. Instead, directly define the hover styles in your main CSS file or use a utility-first approach.  See `bugSolution.css` for an example of how to solve this issue by defining the hover styles directly. 

This issue is likely due to limitations in how `@apply` handles the CSS cascading and pseudo-selectors.  Using utility classes or applying styles more directly within your template provides a more reliable solution.
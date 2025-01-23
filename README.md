# CSS Specificity and !important: An Unexpected Behavior

This repository demonstrates a subtle but important quirk in CSS related to specificity, the `!important` declaration, and inheritance.  The issue occurs when using `!important` to override a style that's inherited through the element's parent.

## The Problem

The core problem lies in how `!important` interacts with inherited styles.  While `!important` is generally used to forcefully override cascading styles, it doesn't necessarily take into account inherited styles in its override process.  This can lead to unexpected results.

## How to Reproduce

1. Clone this repository.
2. Open `bug.css` to see the problematic CSS code.
3. Open `bugSolution.css` to see how it was resolved.
4. Observe that the `<span>` element's `font-size` does not behave as expected in `bug.css`, due to the unexpected interaction of inheritance and the `!important` declaration.

## Solution

The solution involves a better understanding of inheritance and specificity. The `!important` is not the solution, but rather using a more specific selector.
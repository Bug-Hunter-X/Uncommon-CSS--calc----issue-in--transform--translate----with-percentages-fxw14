# Uncommon CSS `calc()` Issue in `transform: translate()` with Percentages

This repository demonstrates an uncommon bug related to the interaction between `calc()`, percentages, and the `transform: translate()` property in CSS.  The bug arises when attempting to position an element using `calc()` to calculate a translation based on a percentage of the element's width.

## Problem

The primary issue stems from the order of operations.  `calc()` computes its value *after* the `transform` is applied.  This unexpected behavior can lead to inaccurate positioning, particularly when the element's size changes dynamically or depends on the layout context.

## Solution

The solution involves rethinking the approach.  Instead of relying on `calc()` within the `translate()` function with percentage based calculations,  it's generally safer and more predictable to use absolute values or adjust the positioning using other CSS properties like `margin`, `left`, or `right` to achieve the desired translation.

## Files

- `bug.css`: Demonstrates the incorrect approach using `calc()` within `translate()`
- `bugSolution.css`: Shows the corrected approach using alternative techniques for positioning
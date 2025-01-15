# CSS `calc()` Function Unexpected Behavior

This repository demonstrates an uncommon issue encountered when using the CSS `calc()` function with percentages and pixel values within nested elements. The unexpected behavior arises from the way `calc()` handles unit conversion and the order of operations.  The example highlights a scenario where subtracting pixels from a percentage width does not produce the intuitively expected result.

## The Problem

The issue stems from how `calc()` interprets the units involved in the calculation.  The subtraction is performed using the element's computed values, which may lead to differences from the expected result if the initial computed value is not what one expects.  This is most often encountered with percentage widths on elements nested within parent containers.

## The Solution

The solution involves restructuring the CSS to avoid relying solely on `calc()` in the context of percentage and pixel subtraction. This might involve explicitly calculating pixel values based on the known container dimensions or using a different approach to achieve the desired layout.
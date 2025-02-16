# JavaScript Bug: Unexpected NaN Result in Addition Function

This repository demonstrates a subtle bug in a JavaScript function that handles addition. The function works correctly with numbers, but it produces an unexpected `NaN` result when one of the input arguments is `NaN`.

## Bug Description

The `foo` function is intended to add two numbers. It correctly handles null values by returning 0.  However, it fails to explicitly handle `NaN` (Not a Number) values, leading to the propagation of `NaN` in the result.  This can be unexpected and difficult to debug, especially in more complex applications.

## How to Reproduce

1. Clone this repository.
2. Open `bug.js`.
3. Run the script using Node.js or a similar JavaScript environment.
4. Observe the unexpected output when `NaN` is used as an input.

## Solution

The solution involves explicitly checking for `NaN` values and handling them appropriately.  This can be done by using `isNaN()` to check the type of the input values.
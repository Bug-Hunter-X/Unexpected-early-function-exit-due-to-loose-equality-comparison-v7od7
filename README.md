# Unexpected Early Function Exit in JavaScript

This repository demonstrates a common, yet subtle, bug in JavaScript related to loose equality (==) comparisons. The `foo` function prematurely exits if either input parameter 'a' or 'b' is null or 0.  The loose equality operator does not distinguish between `null` and 0, thus leading to unintended behavior.

**The bug:** The condition `a == null || b == null` treats 0 as falsy, causing unexpected function termination when 0 is passed as an argument.

**The solution:** The solution is to use strict equality (===) instead of loose equality (==) to correctly check for null values.

## How to reproduce

1. Clone this repository.
2. Open `bug.js` and `bugSolution.js`.
3. Observe the different outputs from testing with null, 0, and other values.

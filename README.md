# Loose Equality Comparison with Null and Undefined in JavaScript

This repository demonstrates a common JavaScript error caused by the loose equality (==) operator when comparing null and undefined values.  The `bug.js` file shows a function with a potential bug, while `bugSolution.js` provides the corrected version.

The issue arises because loose equality does not perform strict type checking.  This can lead to unintended behavior when comparing null and undefined, as they are both considered 'falsy' values.  In the buggy code, the function will prematurely return if either argument is null or undefined, even if the intent is to only handle strictly null values.

The solution involves using strict equality (===) for more precise comparisons.  This ensures that the function only returns if the value is strictly null, avoiding unexpected behavior for undefined values.
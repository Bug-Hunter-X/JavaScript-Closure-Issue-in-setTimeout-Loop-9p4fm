# JavaScript Closure Issue in setTimeout Loop

This repository demonstrates a common JavaScript closure issue that occurs when using `setTimeout` within a loop.  The problem arises because the closure created by `setTimeout` does not capture the value of the loop variable `i` at the time of each iteration, but instead captures it at the end of the loop's execution.

**Problem:** All the `setTimeout` calls will log the final value of `i` (which is 10), instead of 0 to 9 as one might expect.

**Solution:** Use an immediately invoked function expression (IIFE) to create a new scope for each iteration of the loop, thereby capturing the correct value of `i` for each closure.
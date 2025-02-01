# JavaScript Loose Equality Pitfall with null and undefined

This example demonstrates a common pitfall in JavaScript related to loose equality (`==`) when comparing `null` and `undefined`.  The code attempts to handle `null` values gracefully, but fails to do so properly for `undefined`, leading to unexpected `NaN` outputs.

## Bug

The `foo` function intends to return 0 if the input `x` is `null`. However, the loose equality check `x == null` also evaluates to true for `undefined`, causing the function to return `NaN` when called with `undefined`.

## Solution

The solution uses strict equality (`===`) to separately check for `null` and `undefined`, handling them appropriately.

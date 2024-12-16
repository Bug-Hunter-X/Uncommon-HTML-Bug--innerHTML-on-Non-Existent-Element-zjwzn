# Uncommon HTML Bug: innerHTML on Non-Existent Element

This repository demonstrates a subtle HTML bug that might not be immediately obvious. The bug involves attempting to modify the `innerHTML` property of a non-existent element, which silently fails.  Additionally, a style change is performed on a valid element causing an unexpected display outcome.

## Bug Description

The primary bug is the attempt to set `innerHTML` on `'nonExistentElement'`, which does not exist in the HTML structure. A secondary issue hides and shows the correct element, but the initial setting of display:none is not effective due to the erroneous execution of a previous statement.  This leads to the correct element unexpectedly being hidden.

## Solution

The solution involves checking if the element exists before attempting to modify its `innerHTML`. The fix addresses the primary issue, preventing unexpected behavior and ensuring robust error handling. The secondary issue is resolved by rearranging code execution, setting the display property to block immediately following the creation of the element.
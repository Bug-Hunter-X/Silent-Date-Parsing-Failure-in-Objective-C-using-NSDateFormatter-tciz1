# Silent Date Parsing Failure in Objective-C using NSDateFormatter

This repository demonstrates a common but subtle bug in Objective-C when using `NSDateFormatter` to parse dates.  If the input date string doesn't precisely match the `dateFormat` setting of the `NSDateFormatter`, the parsing fails silently and returns `nil`. This can lead to crashes or unexpected behavior in your app, making debugging difficult.

The `bug.m` file shows the problematic code.  The `bugSolution.m` file provides a solution to handle this gracefully.

## How to Reproduce

1. Clone this repository.
2. Open the project in Xcode.
3. Run the app. Observe the error handling (or lack thereof) in the original code.
4. Examine the corrected code in `bugSolution.m` to see how to properly handle potential parsing failures.

## Solution

The solution involves explicitly checking the return value of `dateFromString:` and handling the `nil` case appropriately.  This ensures your app doesn't crash or produce unexpected output when parsing dates.
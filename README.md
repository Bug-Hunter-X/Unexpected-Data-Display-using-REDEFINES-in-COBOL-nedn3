# COBOL REDEFINES Gotcha

This example demonstrates a potential problem when using the `REDEFINES` clause in COBOL to reinterpret numeric data as alphanumeric.  The `DISPLAY` statement will show the internal representation of the data that may not match expectations.

## How to Reproduce

1. Compile and run the `bug.cob` file.
2. Observe the output of the `DISPLAY` statements.  The output does not directly represent the YYYYMMDD date values but rather the underlying internal format.

## Solution

The `bugSolution.cob` file provides a correct approach to handle this type of conversion.  It explicitly defines the data types for the display purpose, ensuring appropriate data representation and readability.
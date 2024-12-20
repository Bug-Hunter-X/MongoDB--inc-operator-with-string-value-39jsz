# MongoDB $inc Operator with String Value

This repository demonstrates a common error when using the `$inc` operator in MongoDB update queries: passing a string value instead of a number.

## Bug Description

The `$inc` operator is used to increment a numeric field by a specified value.  However, if a string is provided as the increment value, the update operation will not work as expected. This often leads to subtle bugs which are difficult to detect.

## Bug Reproduction

The `bug.js` file shows an incorrect usage of the `$inc` operator.

## Solution

The `bugSolution.js` file shows the correct way to use the `$inc` operator with a numeric value. The issue is fixed by ensuring a numerical value is supplied to the `$inc` operator.

## Additional Notes

Careful attention should be paid to the data types used in MongoDB update queries. Type checking and input validation can prevent these types of errors from occurring.
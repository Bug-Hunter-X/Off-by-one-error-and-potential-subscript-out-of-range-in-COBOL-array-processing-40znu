# COBOL Off-by-one Error and Subscript Out-of-Range Example

This repository demonstrates a common error in COBOL programs: an off-by-one error in loop control, combined with the risk of a subscript out-of-range error when accessing an array.  The example highlights how easily these errors can occur and emphasizes the importance of careful array indexing and loop termination conditions in COBOL.

## Bug Description
The `bug.cob` file contains a COBOL program that intends to load data into a table.  However, the loop control in the `PROCEDURE DIVISION` has an off-by-one error. The loop runs from 1 to 100, inclusive, but the table has an upper bound which could cause a runtime error. Additionally, the concatenation in the MOVE statement could lead to unexpected results if not correctly handled, especially when dealing with character string lengths.

## Bug Solution
The `bugSolution.cob` file provides a corrected version of the COBOL program. This corrected version prevents potential runtime errors by rectifying the off-by-one error and ensuring that array subscripts are always within the bounds of the array. The solution ensures that data is correctly loaded into the table.
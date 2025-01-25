# MongoDB $inc Operator Error

This repository demonstrates a common error when using the `$inc` operator in MongoDB update operations. The `$inc` operator is used to increment a numerical field by a specified value.  However, if you provide a string value to `$inc`, MongoDB will likely throw an error or produce unexpected results.

**Bug:** The original code attempts to increment the 'count' field by '10' (a string).  This is incorrect. `$inc` requires a numerical value.

**Solution:**  The corrected code uses a numerical value for the increment.

## How to reproduce

1.  Set up a MongoDB instance.
2.  Create a collection named `myCollection`.
3.  Insert a document with an `_id` and a `count` field (e.g., `{ _id: 1, count: 0 }`).
4.  Run the code in `bug.js`. You'll see an error or incorrect update.
5. Run the code in `bugSolution.js` to see the correct update.
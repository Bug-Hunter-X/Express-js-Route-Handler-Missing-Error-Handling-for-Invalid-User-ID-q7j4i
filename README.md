# Express.js Route Handler Missing Error Handling for Invalid User ID

This repository demonstrates a common error in Express.js route handlers: the lack of proper error handling when dealing with user input.  Specifically, the code attempts to parse a user ID from the request parameters but doesn't handle cases where the ID is not a valid integer.

## Bug

The `bug.js` file contains the flawed code.  The route handler retrieves a user ID from the request parameters and attempts to find a matching user.  However, if the ID is not a number, the `parseInt()` function will return `NaN`, leading to the `users.find()` method potentially failing silently or throwing an error. 

## Solution

The `bugSolution.js` file provides a corrected version of the code. It includes explicit error handling to check if the `userId` is a valid number and to send an appropriate error response if it isn't.

## How to run

1. Clone the repository.
2. Navigate to the repository's directory.
3. Run `npm install express` to install the required package.
4. Execute the code using `node bug.js` or `node bugSolution.js`.
5. Test with various user IDs, including invalid ones, to observe the difference between the buggy and corrected code.
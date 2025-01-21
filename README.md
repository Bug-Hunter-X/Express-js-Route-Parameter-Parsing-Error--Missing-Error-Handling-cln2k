# Express.js Route Parameter Parsing Bug

This repository demonstrates a common bug in Express.js routes where parameters are parsed without proper error handling.  The route `/users/:id` attempts to parse the `:id` parameter as an integer. If the parameter is not a valid integer, or if the parameter is missing altogether, the application will either crash or produce unexpected results.  The solution shows how to correctly handle these scenarios.

## Bug
The `bug.js` file contains the erroneous code.  It attempts to access the user using a potentially invalid user ID without checking or validating the ID's format and existence.

## Solution
The `bugSolution.js` file demonstrates the solution. It includes thorough error handling to check for the following cases:

* **Missing parameter:** Checks if the `id` parameter exists.
* **Invalid parameter:** Validates that `id` is a number using `isNaN()`.
* **User not found:** Handles the case where no user matches the specified ID.

This robust error handling ensures the application behaves gracefully even with incorrect input.
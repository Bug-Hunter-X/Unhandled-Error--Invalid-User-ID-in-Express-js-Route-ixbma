# Express.js Route Handler Bug: Missing Error Handling for Invalid User ID

This repository demonstrates a common bug in Express.js route handlers: the lack of proper error handling when dealing with user inputs, specifically in this case, the user ID.

## Bug Description
The provided code snippet defines an Express.js route that fetches user data based on the ID passed in the URL. However, it lacks crucial error handling for scenarios where the user ID is invalid.  If the `userId` is not a number, attempting to parse it with `parseInt` will lead to unexpected behavior, and ultimately, errors.

## Bug Reproduction
1. Clone the repository.
2. Run `npm install` to install the required dependencies (Express.js).
3. Run the application using `node bug.js`.
4. Send a request to the `/users` route with an invalid user ID (e.g., `/users/abc`).
5. Observe the error or unexpected behavior.

## Solution
The `bugSolution.js` file provides a corrected version of the code that includes comprehensive error handling to address invalid user IDs.  This version checks if `userId` is a number before attempting the parse and handles the case where a user is not found gracefully.

## Learning Points
This demonstrates the importance of robust error handling in Express.js applications.  Always validate and sanitize user inputs to prevent unexpected behavior and potential security vulnerabilities.
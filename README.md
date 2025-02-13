# Express.js Route Handler Missing Error Handling for Invalid User ID

This repository demonstrates a common error in Express.js route handlers:  missing error handling for invalid input.  Specifically, the provided code lacks error handling for non-numeric user IDs.

## Bug
The `bug.js` file contains an Express.js route handler that fetches a user based on their ID.  It attempts to parse the ID as an integer but doesn't handle the case where the ID is not a valid integer, which can lead to runtime errors.

## Solution
The `bugSolution.js` file shows the corrected code with added error handling.  It uses `isNaN` to check if the parsed ID is a valid number and returns a 400 Bad Request error if it's not.
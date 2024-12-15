# Unhandled Promise Rejection in Express.js Async Route

This repository demonstrates a common error in Express.js applications: unhandled promise rejections in asynchronous routes.  When an asynchronous operation within a route handler throws an error, and that error isn't properly caught, the server might crash without providing clear error messages in the logs, making debugging difficult.

## Problem

The `bug.js` file contains an Express.js application with a route that uses a promise.  If the promise rejects (due to the simulated error), the error is not handled, resulting in a silent crash or unhandled rejection warnings.

## Solution

The `bugSolution.js` file provides a corrected version.  It demonstrates proper error handling using a `.catch` block within the route handler. This ensures that errors are logged and that the application remains stable, even if asynchronous operations fail.

## How to reproduce

1. Clone this repository.
2. Navigate to the directory containing `bug.js`.
3. Run the server using `node bug.js`.
4. Observe the server behavior and console output.  The server might crash or show unhandled rejection warnings.
5. Repeat steps 2-4 with `bugSolution.js` to see the corrected behavior.

This example highlights the importance of comprehensive error handling in asynchronous Express.js applications to improve stability and debugging.
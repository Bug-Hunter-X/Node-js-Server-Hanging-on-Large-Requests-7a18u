# Node.js Server Hanging on Large POST Requests

This repository demonstrates a common issue in Node.js where a server hangs on large POST requests if proper error handling isn't implemented.  The `bug.js` file shows the problematic code, while `bugSolution.js` provides the fix.

## Problem

Without proper error handling, the server can fail to respond to large requests, leading to timeouts and unresponsive behavior. This is often caused by exceeding the default buffer limits of the request object.

## Solution

The solution involves adding an 'error' event listener to the request object.  This listener catches potential errors during the request, allowing the server to gracefully handle them and prevent the hang.

## How to Run

1. Clone this repository.
2. Navigate to the repository directory.
3. Run `node bug.js` to see the problematic behavior.  Try sending a large JSON payload to the server using tools like Postman or curl.
4. Run `node bugSolution.js` to see the fixed version in action.

This example highlights the importance of comprehensive error handling in Node.js applications to ensure robustness and stability.
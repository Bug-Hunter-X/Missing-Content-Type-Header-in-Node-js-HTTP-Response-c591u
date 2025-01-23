# Missing Content-Type Header in Node.js HTTP Response

This repository demonstrates a common error in Node.js HTTP servers: omitting the `Content-Type` header in the response.  This can lead to unpredictable client-side behavior, as the client may not correctly interpret the response body.

The `bug.js` file shows the problematic code. The `bugSolution.js` file provides the corrected version.

## How to Reproduce

1. Clone this repository.
2. Navigate to the repository directory.
3. Run `node bug.js`.
4. Make a request to `http://localhost:3000` using a tool like `curl` or a web browser.
5. Observe the client's behavior and compare it to the behavior when running the corrected code in `bugSolution.js`.

## Solution

Always set the `Content-Type` header appropriately to indicate the type of data being sent in the response (e.g., `text/plain`, `application/json`).
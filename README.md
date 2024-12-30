# Node.js Server Port Already in Use

This repository demonstrates a common error in Node.js: attempting to start a server on a port that is already in use.  The `bug.js` file contains the problematic code, while `bugSolution.js` provides a robust solution.

## Problem

The `bug.js` file uses `http.createServer` to create a simple web server.  However, if port 8080 is already occupied by another process, the server will fail to start, resulting in an error.

## Solution

The `bugSolution.js` file addresses this issue by using the `'listening'` event to gracefully handle the case where the port is unavailable.  If the port is in use, a user-friendly message is displayed.  Otherwise, the server starts as expected.
# Node.js Server Unresponsiveness

This repository demonstrates a common issue in Node.js where a long-running synchronous operation in the request handler blocks the event loop, leading to server unresponsiveness.  The `server.js` file contains the buggy code, while `serverSolution.js` provides a solution using asynchronous operations.

## Bug

The `server.js` file shows a simple HTTP server that performs a long-running synchronous operation (a 5-second delay) within the request handler. This blocks the event loop, preventing the server from responding to subsequent requests until the operation completes.  This can lead to a hang or unresponsiveness.

## Solution

The `serverSolution.js` file demonstrates how to avoid blocking the event loop by using asynchronous operations.  This allows the server to continue processing other requests while the long-running operation is in progress.
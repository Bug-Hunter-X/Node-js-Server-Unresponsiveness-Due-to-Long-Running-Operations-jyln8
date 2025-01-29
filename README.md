# Node.js Server Unresponsiveness Due to Long-Running Operations

This repository demonstrates a common issue in Node.js applications where long-running operations within request handlers can cause the server to hang or become unresponsive.  The example uses `setTimeout` to simulate a long operation, but this could represent any computationally expensive task.  The solution shows how to address this using asynchronous programming techniques.

## Bug

The `bug.js` file contains a simple HTTP server that simulates a long-running operation within the request handler.  This causes the server to become unresponsive during the 5-second delay, unable to handle further requests.

## Solution

The `bugSolution.js` file demonstrates how to fix this by using asynchronous functions to handle long-running operations without blocking the main event loop. This allows Node.js to continue processing other requests while the long task is running in the background.
# Unresponsive Node.js Server

This repository demonstrates a common issue in Node.js applications: an unresponsive server caused by a long-running synchronous operation that blocks the event loop.  The `server.js` file contains the buggy code, while `serverSolution.js` provides a corrected version using asynchronous operations.

## Problem

The original code has a synchronous `while` loop that keeps the CPU busy for 5 seconds. During this time, the server cannot accept new requests, resulting in unresponsiveness.

## Solution

The solution uses asynchronous operations to avoid blocking the event loop.  This ensures that the server remains responsive while handling long-running tasks.
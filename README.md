# Unhandled Promise Rejections in Node.js

This repository demonstrates a common, yet easily overlooked, error in Node.js applications: unhandled promise rejections.  Unhandled promise rejections, by default, do not produce any output to the console, making debugging difficult.

## The Problem

The `bug.js` file contains a simple HTTP server.  While this example doesn't explicitly include a promise rejection, it highlights how easily they can occur and go unnoticed.  More complex applications, especially those with asynchronous operations and external API calls, are highly susceptible to this issue.

## The Solution

The `bugSolution.js` file demonstrates the solution: adding an event listener for the `'unhandledRejection'` event.  This listener logs the reason for the rejection and the promise itself, providing valuable information for debugging.

## How to Run

1. Clone this repository.
2. Navigate to the repository's directory.
3. Run `node bug.js` to see the unhandled rejection issue (or lack thereof).
4. Run `node bugSolution.js` to see the improved error handling.
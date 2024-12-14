# React useEffect Hook Memory Leak

This repository demonstrates a common mistake when using the `useEffect` hook in React: forgetting to include a return statement for cleanup. This can lead to memory leaks and unexpected behavior.

## Bug
The `bug.js` file contains a `useEffect` hook that logs a message to the console when the component mounts. However, it's missing a return statement to clean up any side effects when the component unmounts. This means that the log message will continue to be printed even after the component is removed from the DOM, potentially causing memory leaks and performance issues.

## Solution
The `bugSolution.js` file shows the corrected version with a return statement.  The return statement ensures that the log message is no longer printed once the component is unmounted, preventing the memory leak.

## How to reproduce
1. Clone this repository.
2. Run `npm install`.
3. Run `npm start`. 
4. Observe the console logs and the behavior of the component when mounting and unmounting.
# React useEffect setInterval Memory Leak

This repository demonstrates a common error in React applications involving the `useEffect` hook and `setInterval`.  Forgetting to clear the interval in the cleanup function of `useEffect` can lead to memory leaks and unexpected behavior.

## The Bug

The `bug.js` file shows an example of an `useEffect` hook that uses `setInterval` to update a counter every second.  However, it fails to clear the interval before the component unmounts, resulting in a memory leak.

## The Solution

The `bugSolution.js` file demonstrates the correct way to use `setInterval` within `useEffect`.  By storing the return value of `setInterval` and clearing it in the cleanup function, we prevent memory leaks and ensure that the interval is stopped when the component is unmounted.

## How to run

1. Clone this repository.
2. Navigate to the directory in your terminal.
3. Run `npm install`.
4. Run `npm start`.

You can then compare the behavior of the buggy and corrected components. The corrected one handles unmounting cleanly.
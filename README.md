# React useEffect setInterval Memory Leak
This repository demonstrates a common mistake in React applications: using `setInterval` within the `useEffect` hook without proper cleanup.  This leads to memory leaks and performance issues.

## Problem
The `bug.js` file contains a React component that increments a counter every second using `setInterval`. However, it lacks a mechanism to clear the interval when the component unmounts. This causes the interval to continue running even after the component is removed from the DOM, leading to a memory leak.

## Solution
The `bugSolution.js` file demonstrates the corrected implementation. It uses the return value of `useEffect` to clear the interval using `clearInterval` before the component unmounts.  This prevents the memory leak and ensures the application remains performant.
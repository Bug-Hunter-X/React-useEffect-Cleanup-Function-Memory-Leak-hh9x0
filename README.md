# React useEffect Cleanup Function Memory Leak

This repository demonstrates a common mistake in React's `useEffect` hook: forgetting to return a cleanup function. This can lead to memory leaks, especially when dealing with asynchronous operations.

## Bug Description

The provided `MyComponent` uses `useEffect` to log a message on mount. However, it omits a cleanup function, leading to a potential memory leak if the component unmounts before the effect completes.

## Bug Solution

The solution includes a properly implemented `useEffect` hook with a cleanup function that ensures any resources allocated within the effect are released when the component unmounts.  The solution prevents potential memory leaks.
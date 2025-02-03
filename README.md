# Infinite Rerenders in React useEffect Hook

This repository demonstrates a common error in React's `useEffect` hook: infinite rerenders caused by an improperly defined dependency array.

## The Bug
The `MyComponent` function uses `useEffect` to log the current value of the `count` state variable. However, the dependency array is missing `count`, causing the effect to run on every render. This creates an infinite loop, resulting in performance issues or even crashes.

## The Solution
The solution is to include `count` in the dependency array.  This ensures the effect runs only when the value of `count` changes.
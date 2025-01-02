# React useEffect Infinite Render Loop Bug

This repository demonstrates a common bug in React applications involving the `useEffect` hook: an infinite render loop caused by incorrectly managing dependencies.

## Bug Description
The `bug.js` file contains a component that uses the `useEffect` hook to log the render count. However, the dependency array is missing the `count` state variable. This causes the effect to run after every render, triggering another state update and leading to an infinite loop.

## Solution
The `bugSolution.js` file shows the corrected component. By including `count` in the dependency array, the effect only runs when `count` changes, resolving the infinite loop.
# useEffect Runs on Every Render

This repository demonstrates a common error in React's `useEffect` hook where the effect function runs on every render, even when it shouldn't.  The provided solution highlights the correct usage of dependencies to control when the effect runs.

## Problem
The initial implementation of `MyComponent` has an `useEffect` hook that logs the count on every render.  The intention was to only log when the `count` variable changes. This causes unnecessary re-renders and potential performance issues.

## Solution
The solution showcases the proper use of the dependencies array in `useEffect`. By specifying `[count]` as the dependency array, the effect function now only runs when the `count` value changes.
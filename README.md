# React useEffect Infinite Loop Bug

This repository demonstrates a common bug in React applications involving the `useEffect` hook.  The example shows how updating the state variable within the `useEffect`'s dependency array can lead to an infinite loop, causing the component to re-render endlessly.

## Bug Description
The `MyComponent` function uses `useState` to manage a count. The `useEffect` hook, intended to log the count after each update, inadvertently triggers an infinite loop by updating `count` inside the effect, thus causing `useEffect` to run again repeatedly.

## Solution
The solution demonstrates the correct way to use `useEffect` and avoid an infinite loop.  The key is to avoid changing the state within the effect if the dependency already includes the state.
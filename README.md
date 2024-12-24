# React useEffect Hook Bug

This repository demonstrates a common bug in React applications involving the `useEffect` hook.  The bug arises from an improperly defined dependency array, leading to an infinite re-render loop.

## Bug Description
The `MyComponent` component uses `useState` to track a count.  The `useEffect` hook logs the count to the console.  However, the `count` variable is missing from the dependency array. This causes the effect to run after every render, updating the count and triggering another render, creating an infinite loop.

## Solution
The solution is to add `count` to the dependency array in useEffect, ensuring the effect only runs when the `count` value changes.
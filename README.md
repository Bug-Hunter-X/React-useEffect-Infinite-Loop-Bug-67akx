# React useEffect Infinite Loop Bug

This repository demonstrates a common React bug involving an infinite loop within a `useEffect` hook. The bug arises from incorrect logic in handling state updates within the effect's callback.

## Bug Description

The `MyComponent` attempts to reset the `count` state to 0 when it exceeds 5. However, due to the asynchronous nature of state updates in React, the `count` may increment beyond 5 before the state update is reflected.  This leads to the `useEffect` hook continuously triggering, creating an infinite loop.

## Solution

The solution involves ensuring that the state update is processed before triggering the effect again.  This can be done by using functional updates within `setCount` or by using a different approach to control the count.

## How to Reproduce

1. Clone the repository.
2. Run `npm install` to install the dependencies.
3. Run `npm start` to start the development server.
4. Observe the infinite loop behavior in the browser console. 

## How to solve

refer to bugSolution.js file
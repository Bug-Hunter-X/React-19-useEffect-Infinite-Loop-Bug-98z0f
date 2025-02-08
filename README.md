# React 19 useEffect Infinite Loop

This repository demonstrates a common bug in React 19 applications: an infinite loop caused by an incorrectly used `useEffect` hook.  The `useEffect` hook, without a dependency array, runs after every render, leading to an infinite cycle of updates.

## Bug Description
The provided `bug.js` file contains a component that uses `useEffect` without specifying a dependency array. This causes the effect to run every time the component renders, triggering another re-render, and so on.

## Solution
The `bugSolution.js` file presents a corrected version. By adding the `count` variable to the dependency array, the effect only runs when the `count` value changes, resolving the infinite loop.

## How to Reproduce
1. Clone this repository.
2. Run `npm install` to install dependencies.
3. Run `npm start` to start the development server.
4. Observe the infinite loop in the browser's console and potentially a crashing browser.

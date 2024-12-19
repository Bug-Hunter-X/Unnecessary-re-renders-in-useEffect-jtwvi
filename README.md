# Unnecessary Re-renders in React useEffect

This repository demonstrates a common React bug involving unnecessary re-renders within the `useEffect` hook. The `useEffect` hook, without proper dependency array handling, runs after every render, leading to performance issues and potentially unexpected behavior.  The solution showcases how to correctly use the dependency array to optimize the effect's execution.

## Bug

The initial `useEffect` hook in `bug.js` lacks a dependency array. This means it runs after every render, causing the 'Component rendered' message to log repeatedly to the console, even though the component's visual state only changes on button clicks.  This constant re-rendering is inefficient.

## Solution

The corrected version, `bugSolution.js`, adds an empty dependency array `[]` to the `useEffect` hook. This ensures the effect only runs once after the initial render, resolving the unnecessary re-renders and log messages. 
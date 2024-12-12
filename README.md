# React useEffect Dependency Array Issue

This repository demonstrates a common error in React's `useEffect` hook: forgetting to include state variables in the dependency array.  This can lead to unexpected behavior, like infinite re-renders or stale closures. 

The `bug.js` file showcases the problematic code. The `bugSolution.js` file provides the corrected version.

## Problem

The initial implementation of `MyComponent` does not include `count` in the dependency array of `useEffect`. This means that the effect runs after every render regardless of whether `count` has changed.

## Solution

The corrected code includes `count` in the dependency array. This ensures the effect only runs when the value of `count` changes.
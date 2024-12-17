# React useEffect Hook Missing Dependency

This repository demonstrates a common error in React applications: a missing dependency in the `useEffect` hook.  This leads to an infinite loop, where the component constantly re-renders, impacting performance.

## Bug Description

The `useEffect` hook is designed to perform side effects after a render. When dependencies are not specified correctly, it runs on every render cycle, causing unexpected behavior. In this case, it leads to an infinite loop because the effect updates the state, triggering a re-render, triggering the effect again, and so on.

## Solution

The solution involves adding the relevant state variable (in this case `count`) to the dependency array of `useEffect`. This ensures that the effect only runs when the `count` changes.
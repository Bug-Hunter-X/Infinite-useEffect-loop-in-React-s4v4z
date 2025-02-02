# Infinite useEffect Loop in React

This repository demonstrates a common error in React applications involving the `useEffect` hook: creating an infinite loop by omitting or incorrectly specifying the dependency array.

## Problem

The provided `MyComponent` uses `useEffect` to log the current `count` to the console after each render. However, because the dependency array `[]` is empty, the effect runs after every render, regardless of changes to `count`, creating an infinite loop and potentially causing performance problems.

## Solution

The solution involves correctly specifying the `count` variable in the dependency array, causing the effect to run only when `count` changes. 
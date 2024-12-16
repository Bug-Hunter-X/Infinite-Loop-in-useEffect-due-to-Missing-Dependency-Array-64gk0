# React useEffect Infinite Loop Bug

This repository demonstrates a common error in React's `useEffect` hook: an infinite loop caused by a missing dependency array. The component continuously re-renders because the `setCount` function within the `useEffect` hook is called repeatedly without any dependency array to control its execution.  This results in a performance degradation and can lead to application crashes.

## How to Reproduce

Clone this repository and run `npm install` to install the necessary dependencies.  Then, run `npm start` to start the development server. You'll observe that the count continuously increases, indicating the infinite loop.

## Solution

The solution is to add the `count` variable to the dependency array of `useEffect`.  This ensures that the effect is only executed when the `count` variable changes.
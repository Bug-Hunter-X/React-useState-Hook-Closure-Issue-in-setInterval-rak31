# React useState Hook Closure Issue

This repository demonstrates a common issue when using the `useState` hook in React within `setInterval` or other asynchronous operations. The problem arises because the callback function within `setInterval` closes over the initial state value of `count`, rather than the current value. This results in an unexpected behavior where the counter increments by 1 on each interval, but the displayed value remains the same, or jumps unexpectedly. 

## Solution
The solution is to use functional update approach provided by `setCount`.  The functional update takes the previous state as an argument and returns the new state value.   This ensures that you're always working with the most recent state.
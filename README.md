# React useEffect Infinite Loop Bug

This repository demonstrates a common yet subtle bug in React's `useEffect` hook that can lead to infinite loops.  The problem arises from an improperly defined dependency array, causing the effect to run repeatedly and potentially causing performance issues or unexpected behavior.

The `bug.js` file contains the buggy code, while `bugSolution.js` provides the corrected version.  The core issue involves forgetting to include state variables used within the effect in the dependency array.  Failing to do so causes the effect to re-run on every render, creating an infinite loop if the effect modifies the state. 

## How to reproduce

1. Clone this repository.
2. Navigate to the project directory.
3. Run `npm install` to install dependencies.
4. Run `npm start` to start the development server. 
5. Observe the console logs; the buggy version will produce a continuous stream of logs, indicating the effect is running repeatedly, while the solution showcases the corrected version.
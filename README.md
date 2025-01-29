# React setInterval memory leak
This repository demonstrates a common mistake when using `setInterval` within a React component's `useEffect` hook, leading to memory leaks.
The `bug.js` file contains the flawed code, while `bugSolution.js` provides the corrected version.

## Problem
The original code initializes a `setInterval` to update a counter every second. However, it fails to clear the interval when the component unmounts, resulting in continued updates even after the component is no longer rendered. This creates a memory leak, particularly if multiple instances of the component are created and destroyed rapidly.

## Solution
The solution involves using the return value of `useEffect` to clear the interval before the component unmounts. This ensures that the interval is stopped, preventing the memory leak.

## How to Run
1. Clone this repository.
2. Navigate to the project directory: `cd react-setinterval-memory-leak`
3. Install dependencies: `npm install`
4. Start the development server: `npm start`
# Inefficient useEffect Hook in React
This repository demonstrates a common performance issue in React applications involving the `useEffect` hook.

The `bug.js` file contains a component with an `useEffect` hook that runs on every render, causing unnecessary logging and potential performance bottlenecks.  The `bugSolution.js` file provides a corrected version.  The solution utilizes the dependency array to specify what triggers re-runs of the effect.

**Problem:** The original code logs a message on each render, even though this log is only meaningful when the count changes.

**Solution:** Correctly using the dependency array `[count]` in `useEffect` ensures the effect runs only when the `count` state variable changes.
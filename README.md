# React Unhandled Promise Rejection in useEffect

This repository demonstrates a common error in React applications involving unhandled promise rejections within the `useEffect` hook's asynchronous operations.  The initial `bug.js` file showcases the flawed code, while `bugSolution.js` provides the corrected version.

## Problem

The original code attempts to fetch data asynchronously within `useEffect`. However, it fails to properly handle potential errors during the fetch or JSON parsing process.  This can lead to the application silently failing without providing any indication to the user.

## Solution

The solution includes a `catch` block within the `async` function to handle any errors that might occur.  This allows the component to display a user-friendly error message instead of silently failing.  The `finally` block ensures that the loading state is always updated, even if errors occur.
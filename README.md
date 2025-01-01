# React Router Dom Catch-all Route (*) Issue

This repository demonstrates a common issue encountered when using the catch-all route (`/*`) in `react-router-dom`. The problem arises when the catch-all route is placed before more specific routes. In this scenario, the catch-all route will match all paths, preventing other routes from ever being activated.

The `App.js` file contains the buggy code. `AppSolution.js` shows the corrected implementation.

## How to Reproduce

1. Clone this repository.
2. Run `npm install` to install dependencies.
3. Run `npm start` to start the development server.
4. Notice that navigating to `/` or `/about` always shows the 404 page. 

## Solution

The solution involves moving the catch-all route to the end of the `Routes` component to ensure it's matched only when no other routes match.
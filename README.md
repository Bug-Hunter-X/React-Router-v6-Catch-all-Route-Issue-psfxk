# React Router v6 Catch-all Route Issue

This repository demonstrates a common issue in React Router v6 where a catch-all route (`/*`) interferes with other route definitions.  The `/*` route, intended to handle 404 errors, is incorrectly matching all paths before it, preventing other routes from being reached.

## How to Reproduce

1. Clone this repository.
2. Run `npm install` to install dependencies.
3. Run `npm start` to start the development server.
4. Observe that navigating to `/about` results in the 404 page instead of the `/about` component.

## Solution

The solution involves re-ordering routes, placing more specific routes before the catch-all route, ensuring that the catch-all route only matches when no other route matches.  See `AppSolution.js` for the corrected code.
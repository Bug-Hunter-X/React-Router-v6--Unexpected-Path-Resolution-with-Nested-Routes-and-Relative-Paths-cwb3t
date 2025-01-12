# React Router v6: Unexpected Path Resolution with Nested Routes and Relative Paths

This repository demonstrates a subtle bug in `react-router-dom` v6 related to path resolution when using relative paths in deeply nested components.  The issue arises when navigating between sibling routes using relative paths; the paths may resolve incorrectly relative to the application's root instead of the parent route.

## Bug Description

When navigating between sibling routes in deeply nested components using relative paths within `<Link>` components, the path resolution might be incorrect. This leads to unexpected navigation behavior, where the application doesn't navigate to the intended route.

## How to Reproduce

1. Clone this repository.
2. Run `npm install` to install dependencies.
3. Run `npm start` to start the development server.
4. Navigate to the `/parent/child1` route.
5. Click on the link to navigate to `/parent/child2`.  Observe that the navigation may fail.

## Solution

The solution involves using absolute paths instead of relative paths when navigating between routes to ensure correct resolution regardless of nesting level.

## Related Issues

* [React Router GitHub issues](link-to-relevant-github-issues-if-any)

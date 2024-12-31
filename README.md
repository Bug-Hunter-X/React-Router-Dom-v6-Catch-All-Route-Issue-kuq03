# React Router Dom v6 Catch All Route Issue

This repository demonstrates a bug in React Router Dom v6 where the catch-all route (`/*`) always matches, even if another route matches first.  This can lead to unexpected behavior where the 404 page is always displayed.

## To Reproduce

1. Clone this repository.
2. Run `npm install`
3. Run `npm start`
4. Navigate to `/` or `/about`.  The `NotFound` component will still render.

## Solution

The issue is resolved by using a more specific catch-all route that comes after all the other routes.  In this case we simply move the wildcard route to the end of the Routes component.
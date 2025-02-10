# React Router Dom v6 Catch-all Route Issue

This repository demonstrates a problem with catch-all routes (*) in React Router Dom v6.  The issue occurs when a catch-all route is defined, but it fails to trigger when navigating to an invalid URL.

The `bug.js` file contains the problematic code, while `bugSolution.js` provides a working solution.

## Problem

The primary issue is that the catch-all route (`<Route path="*" element={<NoMatch />} />`) does not correctly capture routes that do not match the explicitly defined routes.  This leads to unexpected behavior, such as the page remaining blank or showing previous routes instead of the 404 page.

## Solution

The solution involves a careful review of the Route placement within the Routes component and sometimes requires using the useLocation hook to check against certain route parameters.
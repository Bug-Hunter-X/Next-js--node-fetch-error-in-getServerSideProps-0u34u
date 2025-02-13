# Next.js node-fetch Error in getServerSideProps

This repository demonstrates a common error encountered when using `node-fetch` within the `getServerSideProps` function in a Next.js application.  The error arises because `node-fetch` is not automatically available in the Next.js serverless environment.

## Problem
The `bug.js` file showcases the problematic code. Attempting to use `node-fetch` directly within `getServerSideProps` results in an error during build or runtime.

## Solution
The `bugSolution.js` file provides a corrected version.  Instead of `node-fetch`, it leverages the built-in `fetch` API, which is available within the Next.js serverless environment.  This ensures the code functions correctly without needing additional dependencies.

## How to Reproduce
1. Clone this repository.
2. Run `npm install` to install the dependencies (only necessary for the buggy example).
3. Attempt to run the Next.js development server with the `bug.js` file.
4. Observe the error. Then replace with `bugSolution.js` and run again to see the correct behavior. 
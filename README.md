# React Native: Accessing State/Props Before Component Mount

This repository demonstrates a common error in React Native development: attempting to access component state or props before the component has fully mounted. This leads to undefined values and unexpected behavior.  The repository provides a buggy example and a corrected version.

## Bug Description:

The bug occurs because we attempt to access and use the component's state or props within the constructor or during the initial render, before React has had a chance to set them. This results in the values being undefined, causing errors or unexpected results.

## Solution:

The solution involves using the `useEffect` hook (for functional components) or lifecycle methods (for class components) to ensure that the state and props are accessed only after the component has finished mounting.  This ensures the data is available and prevents errors.

## How to Run:

1. Clone the repository.
2. Navigate to the project directory.
3. Run `npm install` to install dependencies.
4. Run `npx react-native run-android` (or `npx react-native run-ios`) to run the app on your emulator or device.  Then examine the Bug.js and BugSolution.js files to see the difference in how the problem is handled.

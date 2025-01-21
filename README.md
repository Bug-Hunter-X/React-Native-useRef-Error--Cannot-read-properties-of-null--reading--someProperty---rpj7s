# React Native useRef Error: Cannot read properties of null (reading 'someProperty')

This repository demonstrates a common error encountered when using the `useRef` hook in React Native: attempting to access a ref's `current` property before the component has mounted. This results in a runtime error: "Cannot read properties of null (reading 'someProperty')".

## Problem
The provided code attempts to access `myRef.current.someProperty` within the `useEffect` hook. However, if this code runs *before* the component with `ref={myRef}` has mounted, `myRef.current` will be `null`, leading to the error.

## Solution
The solution involves adding a check to ensure that `myRef.current` is not null before attempting to access its properties. This can be done by checking for null or using optional chaining.

## How to Reproduce
1. Clone this repository.
2. Run `npm install` to install dependencies.
3. Run `npx react-native run-android` or `npx react-native run-ios` to start the app.
4. Observe the error in your console.
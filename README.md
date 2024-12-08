# React Native: Accessing State/Props Before Component Mount

This repository demonstrates a common error in React Native development: attempting to access component state or props before the component has fully mounted.  This can lead to undefined values and unexpected behavior.

The `bug.js` file shows the problematic code, while `bugSolution.js` provides a corrected version.

## Problem

Accessing `this.props` or `this.state` within the `constructor` or prematurely in `componentDidMount` can result in undefined values because these properties haven't been fully initialized yet by React.

## Solution

The best solution depends on the context.  If you need to perform an action based on props or state after mounting, always do so within the `componentDidMount` lifecycle method. For data fetched asynchronously, use conditional rendering to display a loading indicator until the data is ready.

## How to run

1. Clone the repository
2. `cd` into the directory
3. `npm install`
4. `npx react-native run-android` or `npx react-native run-ios`
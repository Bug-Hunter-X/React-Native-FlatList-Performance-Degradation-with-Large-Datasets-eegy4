# React Native FlatList Performance Issue

This repository demonstrates a common performance problem encountered when using `FlatList` in React Native with large datasets.  The core issue stems from the absence of a properly configured `keyExtractor` prop.

## Problem

Without a unique key for each item rendered by `FlatList`, React Native struggles to efficiently update the list as it scrolls or when data changes. This leads to slow scrolling, dropped frames, and a generally poor user experience.

## Solution

The solution involves providing a `keyExtractor` function to `FlatList`. This function should return a unique string identifier for each item in your dataset.  This allows React Native to optimize the rendering process significantly.

## Usage

1. Clone this repository.
2. Navigate to the project directory.
3. Run `npm install` to install dependencies.
4. Run `npx react-native run-android` or `npx react-native run-ios` to run the application.

Observe the performance difference between the `bug.js` (incorrect implementation) and `bugSolution.js` (correct implementation) files.

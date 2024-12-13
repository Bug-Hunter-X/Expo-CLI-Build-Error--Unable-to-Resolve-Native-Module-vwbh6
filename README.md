# Expo CLI Build Error: Unresolved Native Module

This repository demonstrates a common issue encountered when using Expo CLI with projects that depend on native modules. The problem arises when a native module isn't properly integrated into the Expo managed workflow, leading to build failures.  The example showcases the error and provides a solution.

## Problem
The `bug.js` file demonstrates a project that attempts to use a native module (`react-native-xyz`, a placeholder) without correct setup for Expo.  Building this project (using `expo build:android` or `expo build:ios`) will result in an error indicating that the module cannot be resolved.

## Solution
The `bugSolution.js` file provides a corrected version.  The solution is often dependent on the specific native module, but generally involves either:

1. **Using an Expo-compatible alternative:**  Search for a compatible library specifically designed for Expo (often marked as such).
2. **Ejecting from Expo:**  Move from the Expo managed workflow to a bare React Native project. This gives you full control over native modules but removes many of Expo's benefits.
3. **Using Expo's `expo install` command:**  If the module is suitable, use `expo install react-native-xyz` to add it. Expo will handle some of the linking.
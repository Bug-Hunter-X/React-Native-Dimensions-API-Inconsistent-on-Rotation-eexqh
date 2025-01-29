# React Native Dimensions API Inconsistency on Rotation

This repository demonstrates a common issue in React Native involving the `Dimensions` API and screen rotation.  The problem lies in the asynchronous nature of the `Dimensions` API's updates. When the device rotates, the returned dimensions may not reflect the new orientation immediately, causing layout discrepancies.

## Bug Description

The `Dimensions.get()` method doesn't instantly update after screen rotation.  This can lead to elements being rendered with incorrect dimensions, resulting in misaligned layouts or clipping.

## Solution

This repository provides a solution that uses the `Dimensions.addEventListener` to listen for changes in screen dimensions and updates the state accordingly.
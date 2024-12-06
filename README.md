# Inconsistent Deep Link Handling with Expo's Linking API

This repository demonstrates a bug in Expo's `Linking` API where the `addEventListener` for deep links does not consistently trigger.  The issue primarily affects scenarios where the app is already running or in the background.

The `linkingBug.js` file showcases the problematic behavior.  The `linkingBugSolution.js` provides a workaround to improve reliability.

## Bug Reproduction

1. Clone this repository.
2. Run the `linkingBug.js` example using Expo Go or a similar environment.
3. Observe that the deep link is not always handled correctly.

## Solution

The `linkingBugSolution.js` provides a more robust solution involving checking for initial URLs and utilizing `getInitialURLAsync` to cover cases where the event listener might miss the initial deep link.
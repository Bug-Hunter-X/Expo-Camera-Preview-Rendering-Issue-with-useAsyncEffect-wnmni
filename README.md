# Expo Camera Preview Rendering Issue

This repository demonstrates a bug where the Expo Camera preview fails to render correctly when used with the `useAsyncEffect` hook. The preview intermittently fails to appear, particularly after screen orientation changes or component remounts.  This issue is not consistently accompanied by clear error messages in the console, making debugging difficult.

## Bug Reproduction

1. Clone this repository.
2. Run `npm install` or `yarn install`.
3. Run `expo start`.
4. Observe the camera preview.  Rotate the device or navigate away and back to the screen to reproduce the issue.

## Solution

The solution involves using the `useEffect` hook with cleanup function. This ensures proper resource management and prevents conflicts that might cause the rendering issues.  The camera component is properly unmounted before remounting, avoiding the preview rendering failure.
# AI-Fitness-Counter

AI fitness tracker that recognizes and counts exercise repetitions. The app lives in the `JumpingJackTracker/` subdirectory — a React Native project that uses the camera and a native MediaPipe pose plugin on iOS to count jumping jacks.

## Prerequisites

1. Complete the [React Native environment setup](https://reactnative.dev/docs/set-up-your-environment) guide (Node, Xcode for iOS, Android Studio if you want Android).
2. Node **≥ 22.11.0** (required by `JumpingJackTracker/package.json`).

## First-time setup

All commands below should be run from the app directory:

```sh
cd JumpingJackTracker
npm install
```

For iOS, install CocoaPods dependencies:

```sh
bundle install
bundle exec pod install --project-directory=ios
```

## Run the app

**Terminal 1 — start Metro:**

```sh
cd JumpingJackTracker
npm start
```

**Terminal 2 — launch on a device or simulator:**

```sh
cd JumpingJackTracker
npm run ios
```

Or open `JumpingJackTracker/ios/JumpingJackTracker.xcworkspace` in Xcode and run from there.

For Android:

```sh
npm run android
```

(Requires an emulator or connected device with USB debugging.)

## Notes

- **Run commands from `JumpingJackTracker/`**, not the repo root. Running `npm install` at the root will not set up the app.
- **iOS is the supported platform for pose detection.** The MediaPipe plugin lives under `ios/FrameProcessorPlugins/`. Android does not have the native plugin yet, so rep counting may not work there.
- **Camera access is required.** Grant permission when prompted. A physical iPhone works best for jumping jacks; the iOS Simulator camera is limited.
- After updating native dependencies, re-run:

  ```sh
  bundle exec pod install --project-directory=ios
  ```

## Troubleshooting

If setup or launch fails, see the [React Native troubleshooting guide](https://reactnative.dev/docs/troubleshooting). Common issues include missing Xcode, CocoaPods not installed, or no iOS simulator selected.

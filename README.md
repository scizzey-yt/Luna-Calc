# Luna Calc

A mobile-first calculator with a custom Luna icon, soft button motion, on-demand answers, keyboard input, and a local calculation history.

## Run the preview

1. Install Node.js if it is not already installed.
2. Run `npm run start` and open the local URL in a browser.

The page is designed for a narrow phone screen and can be installed from a supported mobile browser using **Add to Home screen**.
On iPhone, open the hosted page in Safari, tap **Share**, then **Add to Home Screen**. The app includes an Apple touch icon and standalone display settings.

## Android project

This project includes a Capacitor Android configuration (`com.talha.lumacalc`). After installing Android Studio and its Android SDK:

1. Install Android Studio and its Android SDK, then run `npm install`.
2. Run `npx cap add android` once.
3. Run `npm run android:build` to build a debug APK. The APK appears at `android/app/build/outputs/apk/debug/app-debug.apk`.
4. Open the native project with `npm run android:open` if you want to build or inspect it in Android Studio.

The app has four saved themes, adjustable text and key sizes, optional sound and motion controls, local history, and a branded Luna icon. Calculations appear only after the equals key is pressed. The requested author note and social links live in Settings.

The Android and iOS launcher icons are generated from the Luna mark by `scripts/make-android-icons.ps1`.

An Android SDK/JDK is required to build and install an APK. Calculation history stays on the device. The debug APK is signed with the Android debug key and can be installed directly on a device.

## iOS project

iOS builds require macOS with Xcode and CocoaPods. The `ios/` Xcode project is already generated. On a Mac, run `npm install`, `npm run build`, `npm run ios:sync`, and `npm run ios:open`. In Xcode, choose a simulator or signed device target and use Product → Run or Product → Archive. The web app is also ready to install on iPhone from Safari with **Add to Home Screen**.

This project was prepared on Windows, so it does not include a compiled or signed IPA. Xcode must build and sign the iOS app on macOS.

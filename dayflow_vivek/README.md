# Dayflow by Vivek

A premium, mobile-first to-do planner with four visual themes, an animated creator splash screen, task categories, date navigation, priorities, search, progress tracking, and local-first storage.

## What is included

- `web/` is the offline-capable Progressive Web App (PWA). It can be hosted as a static website and installed from Chrome on Android.
- `android/` is the Android Studio project. It wraps the same app in a lightweight native Android WebView shell and works offline after installation.

## Quick Android install without compiling an APK

1. Host the contents of `web/` on a static HTTPS host such as GitHub Pages or Vercel.
2. Open the hosted site in Chrome on your Android phone.
3. Open Chrome's menu and choose **Install app** or **Add to Home screen**.
4. Dayflow opens in its own app-style window and stores tasks on that device.

The PWA is not an APK file. It is an installable web app.

## Build the APK with Android Studio

1. Open the `android/` folder in Android Studio.
2. Allow Android Studio to install Android SDK Platform 35 and sync Gradle.
3. Select **Build → Build Bundle(s) / APK(s) → Build APK(s)**.
4. Android Studio creates the debug APK at:
   `android/app/build/outputs/apk/debug/app-debug.apk`

The project uses a plain Java Activity and the Android WebView. No paid APIs or accounts are required.

## Build the APK with GitHub Actions

A workflow is included at `.github/workflows/build-apk.yml`. Upload this project to a GitHub repository, open **Actions**, run **Build Dayflow APK**, and download the `dayflow-debug-apk` artifact from the workflow run.

## App details

- App name: Dayflow
- Package ID: `com.vivek.dayflow`
- Version: `1.0.0`
- Minimum Android version: Android 6.0 (API 23)
- Data storage: on-device browser/WebView local storage
- Splash credit: Made by Vivek

## Privacy note

Tasks are stored locally on the device/browser. There is no account, server sync, analytics, or external AI API in this build. Clearing browser/app data can remove locally stored tasks, so use the JSON export in Appearance & data for a backup.

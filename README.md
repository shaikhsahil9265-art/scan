# Roulette Insight Android project

## Build APK using GitHub Actions (phone-friendly)

1. Upload the **contents of this folder** to the root of a GitHub repository. Do not upload this ZIP as the only project file.
2. Ensure `.github/workflows/build-apk.yml` is included (GitHub may hide dot-folders in some mobile file pickers; enable show hidden files if needed).
3. Open the repository's **Actions** tab.
4. Select **Build Android APK**, tap **Run workflow**, then run it on `main`.
5. Open the completed workflow run. Download the artifact named `roulette-insight-debug-apk`.
6. Extract the downloaded artifact ZIP and install `app-debug.apk` on your Android phone. Allow installation from that source if Android asks.

The workflow installs Java 17, Gradle 8.9 and the Android SDK platform/build-tools before building. A successful build cannot be guaranteed until GitHub Actions actually runs; if it fails, open the failed step and inspect its log.

## Local build

Open this folder as an Android project in Android Studio with JDK 17 and Android SDK 35 installed, then build the `assembleDebug` task.

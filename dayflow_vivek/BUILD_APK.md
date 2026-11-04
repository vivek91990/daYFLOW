# Get an APK from GitHub Actions

This project includes a cloud build workflow so the APK can be compiled on a GitHub-hosted Android build machine.

1. Create a new GitHub repository and upload the contents of this folder.
2. Open the repository's **Actions** tab.
3. Select **Build Dayflow APK** and press **Run workflow** (or push a change under `android/`).
4. When the run completes, open it and download the `dayflow-debug-apk` artifact.
5. Extract `app-debug.apk`, send it to your Android phone, and install it. Android may ask you to allow installs from that file/browser app.

For local building, open the `android/` folder in Android Studio, install SDK Platform 35 when prompted, then choose **Build → Build APK(s)**.

This environment did not contain Android SDK/Gradle and cannot reach external package servers, so no compiled `.apk` is included in this bundle. The full Android project and the repeatable build workflow are included.

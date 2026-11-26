# Web App — Android APK project

This repository wraps the supplied HTML app in an Android WebView and builds an APK using GitHub Actions.

## Build the APK on GitHub

1. Create a new GitHub repository.
2. Upload/push all files from this ZIP to the repository (the `.github` folder must be included).
3. Open the repository's **Actions** tab.
4. Select **Build Android APK** and click **Run workflow**, or push a commit to `main`/`master`.
5. When the workflow finishes, open the run and download the **WebApp-debug-apk** artifact.
6. Extract the artifact ZIP to get `app-debug.apk`.

## Notes

- This project builds a **debug APK** for testing/installing. A Play Store release should use a properly signed release build.
- The app loads `app/src/main/assets/index.html` locally. Internet permission is included for online resources used by the HTML (such as Google Fonts).
- App label and Android package ID can be changed in `app/src/main/AndroidManifest.xml` and `app/build.gradle` / `app/src/main/java/...`.

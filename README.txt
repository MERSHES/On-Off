SHAKE TO WAKE — ANDROID SOURCE PROJECT

Important limitation:
This is source code, not an installable APK. It must be built with Android Studio and the Android SDK. This environment does not have the Android build tools needed to compile and test an APK, so an APK is not included and error-free operation cannot honestly be guaranteed.

What it is intended to do:
- Run a foreground service with an ongoing notification.
- Listen for accelerometer movement while Android allows the service and sensor to run.
- Attempt to wake the screen when a shake is detected.
- It never issues a command to power off the phone.

Known limitations:
- It cannot power on a completely shut-down phone.
- Android or the phone manufacturer may suspend sensor delivery while the screen is off, so shake detection may not work reliably on every phone.
- The screen may wake to the lock screen; it does not bypass the PIN, password, or pattern.
- Continuous sensor monitoring can use battery.
- The screen-wake API used here is deprecated by Android and behavior can vary by device and OS version.

Build:
1. Open this folder in a recent Android Studio.
2. Allow Gradle sync and install the Android SDK Platform 35 if prompted.
3. Build > Build Bundle(s) / APK(s) > Build APK(s).
4. Install the resulting APK on your phone.
5. Open Shake to Wake and tap Enable shake detection.
6. Use Stop shake detection or force-stop the app to stop it.

This project has not been compiled or tested on the user's phone.
AUTOMATED BUILD OPTION (GitHub Actions):
1. Extract this ZIP.
2. Create a GitHub repository and upload the extracted project files, including the hidden .github folder.
3. Open the repository's Actions tab.
4. Run "Build Shake to Wake APK" (or push to the main branch).
5. When the workflow succeeds, open that run and download the "ShakeToWake-debug-apk" artifact.
6. Extract the artifact ZIP to get app-debug.apk, then transfer it to your Android phone and install it.
GitHub account/repository setup is required. The workflow has not been run from this environment.

# Pencil Circuit (Android)

A full-screen Android app that runs the Pencil Circuit game offline. The game, the 3D library and the fonts are all inside the app (`app/src/main/assets`), so it needs no internet and asks for no permissions.

## Get the APK

### Option 1: Android Studio (easiest)
1. Install Android Studio and open this folder.
2. Wait for the Gradle sync to finish.
3. Choose **Build > Build Bundle(s) / APK(s) > Build APK(s)**.
4. The file is at `app/build/outputs/apk/debug/app-debug.apk`. Copy it to your phone and open it.

### Option 2: GitHub (no install on your computer)
1. Create a new GitHub repository and upload everything in this folder, including the hidden `.github` folder.
2. Open the **Actions** tab, choose **Build APK**, and press **Run workflow**.
3. When it finishes, download `pencil-circuit-apk` from the run page. It contains `app-debug.apk`.

### Option 3: Command line
With the Android SDK and Gradle 8.7 or newer installed:

```
gradle assembleDebug
```

## Installing on the phone
Open the APK on the phone. Android will ask to allow installs from that app (Files, Chrome, etc.). This is a debug-signed build for personal use. To publish on Google Play you need a release build signed with your own key.

## Changing the game
The whole game is `app/src/main/assets/index.html`. Edit it, rebuild, and reinstall.

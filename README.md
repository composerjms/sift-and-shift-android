# Sift & Shift for Android

The single-file game (`www/index.html`) wrapped as an Android app with Capacitor 6.

## Getting a build
Every push to `main` builds an APK on GitHub Actions and publishes it under **Releases**.
On the tablet: open the latest release in Chrome, tap the `.apk`, and install
(Android asks once to allow installs from Chrome). Installing a newer build over an older one keeps the saves.

## What the app adds
- Saves live in the app's own storage (not Chrome's), so clearing Chrome doesn't touch them. Uninstalling the app does.
- Save codes, milestone saves and test logs open the share sheet (save to Files, Drive, email...).
- The screen stays on while the game is in front.
- Time away (switching apps, screen off) goes into the offline bank when you come back.
- Back pauses; Back twice within 2 seconds saves and closes.

## Updating the game
Replace `www/index.html` with the new build of the game and push.

## Signing
`android/app/sift-sideload.keystore` is a fixed key for personal sideloading only, so each build can update the last one.
It is not a Play Store key.

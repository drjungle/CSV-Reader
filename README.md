# CSV Reader (Android)

The page that runs inside the app is `www/index.html` (edit settings at the top of its script).

## Build the APK without installing anything (GitHub)
1. Create a new GitHub repository and upload everything in this folder (keep the `.github` folder).
2. Open the repository's **Actions** tab → **Build APK** → wait for the green check (about 5 minutes).
3. Open that run and download **csv-reader-apk** (a zip containing `app-debug.apk`).
4. Copy `app-debug.apk` to your phone and open it. Allow "install unknown apps" when Android asks.

## Build it on your own PC
Needs Node 18+, JDK 17 and Android Studio (or the Android SDK).
    npm ci
    npx cap sync android
    cd android
    gradlew assembleDebug        (Windows)   |   ./gradlew assembleDebug   (Mac/Linux)
The APK is created at `android/app/build/outputs/apk/debug/app-debug.apk`.
Or run `npx cap open android` and use Build > Build APK(s) in Android Studio.

After changing `www/index.html`, run `npx cap sync android` before building again.

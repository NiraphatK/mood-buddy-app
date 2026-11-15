# Mood Buddy

*Track your emotions. Understand yourself better.*

**Mood Buddy** is a native Android application built with **Java** in **Android Studio**. It helps users log and reflect on their daily moods, promoting emotional awareness and mental well-being. The app uses **Firebase** for secure authentication and real-time data synchronization.

## Features

- Log your **daily mood** with optional personal notes
- Browse your **mood history** in a clean, chronological timeline
- Secure **login and registration** with [Firebase Authentication](https://firebase.google.com/products/auth)
- **Real-time data syncing** with [Firebase Realtime Database](https://firebase.google.com/products/realtime-database)

## Built With

- [Java](https://www.oracle.com/java/) — Programming language for native Android development
- [Android Studio](https://developer.android.com/studio) — Official IDE for Android app development
- [Firebase Authentication](https://firebase.google.com/products/auth) — Secure user management
- [Firebase Realtime Database](https://firebase.google.com/products/realtime-database) — Cloud-hosted NoSQL database

## Build and run

### Requirements

- Android Studio with support for Android Gradle Plugin 8.9.0 and JDK 17 for Gradle.
- Android SDK Platform 35 and an Android 15 / API 35 emulator or device. The committed app sets **minSdk, targetSdk, and compileSdk to 35**.
- Your own Firebase project with Email/Password Authentication and Realtime Database enabled.

### Firebase configuration

1. Register an Android app in your Firebase project using application ID `com.example.final_project`.
2. Download that project's `google-services.json` into `app/google-services.json`. Use your own configuration and keep private credentials/service-account files out of Git.
3. Enable Email/Password in Firebase Authentication and create a Realtime Database.
4. Review the reads/writes under the `users` node in the app code and configure database rules for the intended authenticated access. Do not make the database publicly readable/writable to bypass setup errors.

### Start the app

```bash
git clone https://github.com/NiraphatK/mood-buddy-app.git
cd mood-buddy-app
```

Open the repository root in Android Studio, let Gradle sync, select an API 35 device, and run the `app` configuration. On macOS/Linux, a command-line debug build is:

```bash
bash ./gradlew assembleDebug
```

On Windows:

```powershell
.\gradlew.bat assembleDebug
```

The debug APK is generated under `app/build/outputs/apk/debug/`. Register a test account, save a mood, and confirm that history reloads. Use synthetic notes while checking your Firebase rules. Firebase setup and a device smoke test must be completed on your own project; they were not validated by this documentation update.

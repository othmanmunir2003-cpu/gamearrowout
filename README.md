# Arrow Out - Android Packaging Guide

This guide outlines the steps to package your "Arrow Out" web game as an Android APK using [Capacitor](https://capacitorjs.com/).

## Prerequisites
Ensure you have the following installed on your computer:
1. **Node.js**: [Download and install](https://nodejs.org/) (LTS version recommended).
2. **Android Studio**: [Download and install](https://developer.android.com/studio) to build the APK.

## Setup Steps

### 1. Initialize the Project
Open your terminal/command prompt, navigate to your project folder (`C:\Users\munir\Desktop\arrow out`), and run:

```bash
npm init -y
npm install @capacitor/core @capacitor/cli
npx cap init ArrowOut com.example.arrowout --web-dir www
```

### 2. Add Android Platform
Run the following command to add the Android platform to your project:

```bash
npm install @capacitor/android
npx cap add android
```

### 3. Update the App Icon
Capacitor requires specific icon sizes. You can use the [Capacitor Assets](https://github.com/ionic-team/capacitor-assets) tool to automatically generate all required icon sizes from your `assets/icon.png`.

```bash
npm install @capacitor/assets --save-dev
npx cap-assets generate --icon assets/icon.png
```

### 4. Build and Sync
Whenever you make changes to your files in the `www` folder, sync them to the Android project:

```bash
npx cap sync
```

### 5. Build the APK in Android Studio
1. Open the Android project in Android Studio:
   ```bash
   npx cap open android
   ```
2. Once Android Studio opens, wait for the project to finish building.
3. In the top menu, go to **Build** > **Build Bundle(s) / APK(s)** > **Build APK(s)**.
4. Android Studio will build the APK and notify you when it's ready, providing a link to locate it.

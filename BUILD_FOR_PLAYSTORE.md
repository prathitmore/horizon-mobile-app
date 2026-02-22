# How to Build Your App for Google Play Store

The Android project for **Orivex Horizon** is fully generated and ready in this folder.
However, to build the final APK or App Bundle (.aab) for the Play Store, you need **Java 17** (currently you have Java 8).

## Step 1: Install Java 17
1.  Download **Java 17 JDK** from here: [https://adoptium.net/temurin/releases/?version=17](https://adoptium.net/temurin/releases/?version=17)
2.  Install it and ensure you check the option "Set JAVA_HOME variable".
3.  Restart your computer (or just your terminal).

## Step 2: Build the App
1.  Open your terminal in this `HorizonMobile` folder.
2.  Run the following command to generate the **App Bundle (.aab)** (Required for Play Store):
    ```powershell
    cd android
    .\gradlew bundleRelease
    ```
    *Note: Use `bundleRelease` for Play Store, and `assembleDebug` for testing on your phone.*

3.  Once finished, your file will be at:
    `android/app/build/outputs/bundle/release/app-release.aab`

## Step 3: Sign & Upload
- You will need to sign this bundle using your **Keystore** before solving it to Google Play Console.
- You can do this easily by opening the `android` folder in **Android Studio** if you wish, using "Build > Generate Signed Bundle / APK".

Your code is ready. You just need the correct Java version to compile it!

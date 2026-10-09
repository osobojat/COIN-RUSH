# Coin Rush — Android starter project

A portrait Android arcade game using a local HTML5 Canvas game inside an Android WebView, with a Google AdMob banner placement.

## Included
- Touch-first coin-collecting game with 30-second rounds
- Bombs subtract time; coins add to a local virtual wallet
- Locally saved best score and virtual coin total
- AdMob banner configured with Google's **test** ad unit
- No cash payouts, accounts, payment handling, or real-money rewards

## Build an APK

You need Android Studio (current stable), JDK 17, and Android SDK Platform 35.

1. Extract this ZIP.
2. Open the `CoinRushAndroid` folder in Android Studio.
3. Allow Gradle sync and install any requested Android SDK components.
4. To build a debug APK, choose **Build → Build Bundle(s) / APK(s) → Build APK(s)**.
5. Android Studio will show the APK location, normally `app/build/outputs/apk/debug/app-debug.apk`.
6. Install that debug APK on your Android phone for testing. For release, use **Build → Generate Signed Bundle / APK**.

This source ZIP is a project, not a precompiled APK. No APK has been built or tested on a physical phone by this package-generation step.

## Before publishing or earning ad revenue

1. Create an app in your own Google AdMob account.
2. Replace the sample AdMob **App ID** in `app/src/main/AndroidManifest.xml` with your own App ID.
3. Replace the sample banner ad unit ID in `app/src/main/java/com/coinrush/arcade/MainActivity.kt` with your own banner ad unit ID.
4. Keep Google's test IDs during development. Never click your own live ads; test with test ads until the app is ready.
5. Add a privacy policy and complete the Google Play Data safety, ads, content rating, and other required declarations accurately. Review consent requirements for your audience and regions; integrate a certified consent flow if applicable.
6. Review Google Play's current target API requirement and update `targetSdk` before submission if needed.
7. Test on multiple Android devices and check gameplay, ad loading, network/offline behavior, and lifecycle behavior.
8. Generate a signed Android App Bundle (AAB) for Google Play. A debug APK is for testing, not Play Store release.

## Important limitations
- Ads and revenue are not guaranteed; earnings depend on eligible traffic, geography, fill, ad format, and policy compliance.
- The wallet is local-only and virtual. It cannot be redeemed for money.
- The included AdMob identifiers are Google's sample test identifiers, not monetization credentials.
- This starter does not include a privacy-policy website, analytics, cloud saves, or an in-app consent SDK.
- Check current Google AdMob and Google Play policies before release. Do not encourage accidental ad clicks or show ads in a way that disrupts gameplay.

## Build without owning a computer (GitHub Actions)

This repository includes `.github/workflows/android.yml` to build a **debug APK in GitHub's cloud**.

1. On your Android phone, sign in to GitHub and create a new repository.
2. Upload the project files from this ZIP into the repository, preserving folders (including `.github/workflows/android.yml`). GitHub's mobile browser upload UI may be easier in desktop-site mode.
3. Open the repository's **Actions** tab and select **Build Coin Rush APK**. If prompted, enable Actions and tap **Run workflow**.
4. When the run succeeds, open the run and download the `CoinRush-debug-APK` artifact. GitHub may download it as a ZIP; extract it to get `app-debug.apk`.
5. Open the APK on your phone and allow installs from that source if Android asks.

This workflow builds a **debug/test APK**, not a signed production release. Do not upload signing passwords or AdMob credentials to a public repository. The app currently uses Google's sample test ad identifiers.

# Android port status

## Current state

This repository already contains the upstream SuperTuxKart Android build system. This is not a blank Android port.

Verified files:
- `android/ANDROID.md` — Android build guide.
- `android/make.sh` — APK build orchestration.
- `android/make_deps.sh` — native dependency builds for Android ABIs.
- `android/generate_assets.sh` — packages and optimizes game assets.
- `android/build.gradle` — Android Gradle Plugin configuration.
- `android/Android.mk` — NDK native build definitions.
- `android/AndroidManifest.xml` — Android app manifest.
- `android/gradle/wrapper/gradle-wrapper.properties` — Gradle wrapper distribution.

## Supported configuration declared by the build scripts

- Minimum Android SDK: 21 (Android 5.0).
- Target SDK: 35.
- NDK: 28.1.13356709.
- ABIs: armeabi-v7a, arm64-v8a, x86, x86_64.
- Gradle Android plugin: 8.7.3.
- Gradle wrapper: 8.9.

## Remaining build inputs

The documented build requires:
1. Android SDK and the specified NDK.
2. The matching `dependencies-android-src` archive extracted under `lib/`.
3. The separate `stk-assets` content tree.
4. Linux build tools and Python packages listed in `android/ANDROID.md`.

## Verification status

- Repository files inspected: Android guide, Gradle config, manifest, NDK makefile and build scripts.
- No APK has been built in this session.
- No emulator or physical-device test has been run.
- Multiplayer has not been runtime-tested.

## Next steps

1. Verify the exact source revision and matching assets/dependency package.
2. Run the debug build for `arm64-v8a` first.
3. Fix reproducible build errors without changing upstream gameplay code unnecessarily.
4. Install and test on a physical Android device.
5. Test touch controls, graphics, audio, suspend/resume and online connectivity.

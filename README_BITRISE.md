# NEXVIA — Bitrise build package

This package is prepared for Bitrise. The Bitrise workflow deliberately does **not** depend on `gradle-wrapper.jar`.
Instead, the workflow downloads the pinned Gradle 8.9 distribution and runs `:app:assembleDebug`, then uploads `app-debug.apk` to Bitrise Artifacts.

## What to do

1. Replace the files in your GitHub repository with the contents of this folder.
2. In Bitrise, use the `build_apk` workflow.
3. Run the build.
4. Download `app-debug.apk` from the Artifacts tab.

The workflow also contains a push trigger for all branches.

Note: this APK is still the NEXVIA starter app. The VPN button is a UI demo; real WireGuard/API connectivity has not yet been added.

# Wolf Countdown — Android source

Native Android countdown app with a black-and-gold wolf identity.

## Features
- Target date and optional goal name.
- Calendar-day countdown, including dates that have passed.
- Daily on-device reminder at the selected time.
- Alarm sound, notification sound, or silent reminder channel.
- Local-only storage; no internet permission.
- Re-schedules reminders after reboot.
- Wolf artwork launcher icon.

## Build an APK using only your Android phone (GitHub cloud build)
This is source code, not an APK. The included GitHub Actions workflow builds a debug APK in the cloud, so a computer is not required. You need a GitHub account and an internet connection for the build/download steps.

1. On your phone, open https://github.com and sign in or create an account.
2. Create a **new repository** named `WolfCountdownAndroid`. Choose **Public** for the simplest setup, or use a private repository if you prefer.
3. In the repository, upload the project files and folders from this ZIP. GitHub's mobile browser may be easier with **Request desktop site** enabled. Make sure `.github/workflows/build-apk.yml` is uploaded; hidden folders beginning with a dot can be easy to miss.
4. Commit the files to the `main` branch.
5. Open the repository's **Actions** tab. Select **Build Wolf Countdown APK** and tap **Run workflow** if it has not started automatically.
6. Wait for the workflow to finish successfully. Open that completed run and find **Artifacts** near the bottom.
7. Download `WolfCountdown-debug-apk`. GitHub may download it as a ZIP; extract it in your phone's Files app to get `app-debug.apk`.
8. Tap `app-debug.apk` and follow Android's installation prompts. If prompted, allow your browser or Files app to **Install unknown apps** for this installation.
9. Open Wolf Countdown, allow notifications, choose your target date/time/sound, and tap Save.

## Notes
- The workflow compiles the project and uploads a debug APK; it does not publish the app to an app store.
- Countdown and alarms work without internet after installation. Android 13+ needs notification permission. Android battery restrictions can affect delivery.
- On Android 8+, sound is controlled by notification-channel settings; if you change a channel sound in Android Settings, the OS may keep that override.

# Privacy Policy — GymLock

_Last updated: 2026-07-11_

GymLock ("the app") is developed by Nihal Rasekar. This policy explains what the app accesses and, more importantly, what it does **not** do with it.

## Summary

GymLock does not collect, store, transmit, or share any personal data with the developer or any third party. All processing happens entirely on your device. The app has no servers, no analytics, and no advertising SDKs.

## Permissions and why the app needs them

| Permission | Purpose |
|---|---|
| Camera | Used only while you are on the Exercise screen, to run on-device pose detection  that counts your push-ups. No photo or video is ever saved, recorded, or sent anywhere. |
| Activity Recognition | Used to count your steps so they can be converted into earned screen time. |
| Accessibility Service | Used to detect which app is currently in the foreground, so GymLock can show the exercise/lock screen when you open an app you've chosen to lock. GymLock does not read, log, or transmit the content of any app, only the package name of the app in the foreground. |
| Post Notifications | Used to show the persistent "time remaining" / step-count notification while a lock/timer session is active. |
| Foreground Service (Special Use) | Used to keep the step counter and time-bank countdown running reliably in the background while a session is active. |
| Wake Lock | Used briefly to keep step counting accurate while the screen is off. |
| Ignore Battery Optimizations (request) | Optional — you may be asked to exempt GymLock from battery optimization so locking/step-counting continues to work reliably in the background. |

## Data storage

Your settings (which apps are locked, your earned time bank, step counts) are stored only in local app storage on your device, using Android's standard app preferences mechanism. This data is deleted automatically if you uninstall the app, and is included in Android's normal device backup only if you have backup enabled (`android:allowBackup="true"`), which stays under your Google account's control, not the developer's.

## Children's privacy

GymLock does not knowingly collect data from anyone, including children, because it does not collect data at all.

## Changes to this policy

If this policy changes, the updated version will be posted at this same URL with a new "Last updated" date.

## Contact

truetech988@gmail.com

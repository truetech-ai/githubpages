# Play Console — copy-paste answers

Fill [YOUR NAME], [YOUR CONTACT EMAIL], hosted privacy policy URL before submit. Privacy policy must be hosted at a public URL (GitHub Pages, Notion public page, or plain webpage) — Play Console will not accept a local file, upload `privacy-policy.md` content somewhere public and paste that URL in the two spots below.

## 1. App content → Privacy policy
Paste the hosted URL of `privacy-policy.md`.

## 2. App content → Permissions declaration form (Accessibility API)
**Core functionality this app provides that requires the Accessibility API:**
> GymLock is an app-locking / gamified screen-time app. It lets the user choose specific apps to lock behind an exercise or step-count challenge. To detect when the user opens a locked app (so the lock/challenge screen can be shown), GymLock must know which app is currently in the foreground. The Android Accessibility API's `TYPE_WINDOW_STATE_CHANGED` event is the only public API that provides this. The service only reads the foreground app's package name — `canRetrieveWindowContent` is set to `false`, no screen content, text, or window hierarchy is ever read, logged, or transmitted.

**Why a less invasive API/permission won't work:**
> `UsageStatsManager` (usage-access) only provides historical/polled usage data with several-second latency and requires the user grant a separate special permission with no advantage in transparency; it cannot reliably catch fast app switches in real time the way an accessibility event does, which is required to show the lock screen before the locked app's UI is interacted with.

## 3. App content → Foreground service permission declaration (specialUse)
Use for both `StepCounterService` and `TimeBankCountdownService`:
> These foreground services keep step-counting and the earned-screen-time countdown running reliably while the app is in active use (screen off or another app in foreground), so time bank deductions and step-to-minutes conversion stay accurate. They do not sync or transfer data anywhere; everything is on-device.

## 4. App content → Data safety form
Answer **"No data collected"** for every category (Location, Personal info, Financial, Health & fitness, Messages, Photos/videos, Audio, Files/docs, Calendar, Contacts, App activity, App info/performance, Device/other IDs). This is accurate because:
- Camera frames are processed in-memory by ML Kit and discarded, never saved or transmitted.
- Step counts / locked-app list / time bank are stored only in local `SharedPreferences`.
- No network calls, no analytics SDK, no ad SDK exist in the app (verified — no `http`, `okhttp`, `Firebase`, `Analytics` in code).

If asked "Is all user data encrypted in transit?" → answer **N/A / not applicable**, since no data leaves the device.

## 5. App content → Target audience & content
Not fitness-medical advice; pick age group per your judgment (likely 13+ given step/exercise gamification, unless you're targeting kids — if so, additional Families policy requirements apply, different form).

## 6. Ads
Declare **No ads** (no ad SDK found in dependencies).

## 7. Government apps / News / COVID-19 apps
Not applicable — skip.

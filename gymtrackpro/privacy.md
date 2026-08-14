---
layout: default
title: Privacy Policy — GymTrack Pro
---

# Privacy Policy

**Effective date:** 20 April 2026
**Last updated:** 20 April 2026
**App:** GymTrack Pro (iOS)
**Developer:** D. Raj Gurung
**Contact:** [divy5831@gmail.com](mailto:divy5831@gmail.com)

This Privacy Policy describes how GymTrack Pro ("the app," "we," "our," or "us") handles information when you use the iOS application. We believe your workout data belongs to you and should stay with you. This policy explains, in plain language, what that means in practice.

---

## 1. Our privacy principles

GymTrack Pro is built with the following commitments:

1. **Your data is yours.** All workout information, profile details, and logs are stored on your device by default.
2. **No third-party tracking.** The app does not include advertising SDKs, analytics SDKs, crash reporting that identifies users, social login tracking, or any third-party data brokers.
3. **No server backend.** We do not operate a server that receives your data. Optional cloud sync uses **your own iCloud account**, not ours.
4. **No sale of data.** We do not sell, rent, or lease any user information to any third party, ever.
5. **Minimum collection.** We only ask for the information the app needs to function.

---

## 2. Information we handle

### 2.1 Information you provide directly

When you use the app, you may create or enter:

- **Profile information** — your name, preferred weight unit (kg/lb), fitness experience level, fitness goal, and optional profile photo.
- **Workout plans** — the workout splits you select or build (e.g. Push/Pull/Legs, Upper/Lower), the exercises in each day, and your schedule.
- **Workout logs** — sets, reps, weight, Rate of Perceived Exertion (RPE), notes, rest timer data, workout duration, and timestamps.
- **Body weight entries** — if you choose to log them manually.

All of this is stored **locally on your device** using Apple's SwiftData framework.

### 2.2 Information the app reads with your permission

With your explicit consent (granted through the standard iOS permission prompts), the app may access:

- **Apple Health (HealthKit)** — only if you enable the integration. The app can:
  - *Read* your body weight entries so your progress charts stay in sync with the Health app.
  - *Write* completed workouts to the Health app as "Traditional Strength Training" activities, including estimated duration and energy burned.
  - The app does **not** read or request heart rate, steps, sleep, location, or any other health data outside body weight and workouts it created.
- **Photo Library** — only if you tap "Edit Profile" and choose to pick a profile picture. The selected image is stored locally and, if iCloud sync is enabled, in your private iCloud database. We do not scan, analyse, or transmit the image anywhere else.

You can revoke either permission at any time in **Settings → Privacy & Security → Health** or **Settings → Privacy & Security → Photos → GymTrack Pro**.

### 2.3 Information Apple's frameworks may access automatically

Because GymTrack Pro runs on iOS, the following standard iOS APIs are used. These are documented in our machine-readable privacy manifest (`PrivacyInfo.xcprivacy`) that ships inside the app:

| API | Why we use it |
|---|---|
| `UserDefaults` | Store your preferences (weight unit, week start day, theme choices). |
| File timestamps | Display when workouts happened and sort history chronologically. |
| System boot time | Measure elapsed time during a workout (rest timers, total duration). |
| Available disk space | Make sure your workout logs can be saved before writing. |

None of this data leaves your device.

### 2.4 Information we do NOT collect

For clarity, GymTrack Pro does **not** collect or process any of the following:

- Precise or coarse location
- Device identifiers (IDFA, IDFV, advertising IDs)
- Contacts, calendar events, camera (beyond your explicit photo-library pick), microphone, or audio
- IP address, MAC address, or network metadata
- Payment information (the app has no paid features or in-app purchases at this time)
- Browsing history, search queries, or URLs
- Phone numbers
- Health data beyond what Section 2.2 describes
- Demographic data beyond what you enter into your profile

---

## 3. How your information is used

We use the information described in Section 2 strictly to power app features you requested:

- Display your workout history, progress charts, and personal records.
- Calculate 1-rep-max estimates, total volume, and streak counters.
- Show relevant exercise suggestions based on your fitness goal and experience level.
- Send you local notifications for rest timers and scheduled workouts **only on your device** — no server is involved.
- Write completed workouts to Apple Health if you've enabled the HealthKit integration.
- Sync your data between your devices via your iCloud account if you've enabled iCloud sync.

We do **not** use your data for advertising, marketing, profiling, behavioural analysis, research, model training, or any purpose unrelated to running the app.

---

## 4. How your information is stored and synced

### 4.1 Local storage (always)

All of your workout data, profile, and settings live on your iPhone inside the app's sandboxed storage, managed by Apple's SwiftData framework. This storage is encrypted at rest by iOS when your device passcode is set, and protected by iOS Data Protection.

### 4.2 Optional iCloud sync (opt-in)

GymTrack Pro supports syncing data between your Apple devices (iPhone, Apple Watch companion app, widgets) using **CloudKit**. If you enable iCloud sync:

- Your data is stored in the **private database of your personal iCloud account**, not on our servers.
- We, as the app developer, have **no access** to your iCloud data. Apple's architecture enforces this — the private database is readable only by your Apple ID.
- Data in transit is encrypted via TLS (provided automatically by Apple).
- Data at rest in iCloud is encrypted by Apple per [Apple's iCloud security overview](https://support.apple.com/guide/security/icloud-data-security-overview-sec0b2ea2a5d/web).
- If you disable iCloud sync, the app continues to work with local-only storage. If you delete the app or sign out of iCloud, your cloud copy may be removed by iCloud according to Apple's retention rules.

### 4.3 Apple Watch + Widgets

If you use the Apple Watch companion or home-screen widgets, they share a small subset of your data (the active workout session and today's stats) through an **App Group container** scoped to your device. This data is never transmitted off your device, except as part of the iCloud sync described above.

### 4.4 Apple Health

Workouts written to Apple Health become part of your Health database, which is governed by [Apple's Health & Privacy terms](https://www.apple.com/legal/privacy/) — not by GymTrack Pro. You can delete any workout we wrote by opening the Health app → Browse → Workouts.

---

## 5. Sharing and disclosure

We do not share, sell, trade, or disclose your personal information to third parties, except in the narrow cases below:

- **With Apple (automatically)** — via iCloud, HealthKit, and standard iOS APIs, subject to Apple's privacy terms. Apple's role here is as your **data processor**, not ours.
- **Legal obligation** — if we receive a valid legal request, we would comply as required by law. Because we do not operate a server or hold your data, there is nothing for us to disclose — all such requests would need to be directed to Apple for iCloud data.
- **Aggregate, non-identifying analytics** — we do not currently collect any. If we ever add such analytics, this policy will be updated and you will be given the option to opt out before any collection begins.

We do not use your data to train machine learning models.

---

## 6. Your rights

### 6.1 Access, correction, export, and deletion

Because your data is stored locally on your device (and optionally in your own iCloud account), you have direct, unmediated control at all times:

- **Access:** all of your data is visible in the app's History, Progress, and Profile tabs.
- **Correction:** edit profile fields in Profile → Edit Profile; edit workouts in History → tap a session.
- **Export:** export a JSON file of your data from Profile → Settings → Export Data.
- **Deletion:** delete individual workouts from the History tab; reset all data from Profile → Settings → Reset; or simply uninstall the app to remove local data. If you've enabled iCloud sync, delete your cloud copy in **iOS Settings → \[your name\] → iCloud → Manage Storage → GymTrack Pro → Delete Data**.

### 6.2 Rights under GDPR (European Economic Area, UK, Switzerland)

If you are in the EEA, UK, or Switzerland, you have the rights of access, rectification, erasure, restriction of processing, data portability, and objection under the GDPR/UK GDPR. As described above, the app architecture puts all of these controls directly in your hands. If you have additional questions, contact us at [divy5831@gmail.com](mailto:divy5831@gmail.com).

### 6.3 Rights under CCPA/CPRA (California residents)

If you are a California resident, you have the rights of access, deletion, correction, opt-out of sale, and non-discrimination under the CCPA/CPRA. GymTrack Pro does **not sell or share** personal information in the sense defined by these laws. You may still exercise access/deletion rights as described in Section 6.1, or contact us directly.

### 6.4 Other regions

Users in Brazil (LGPD), Canada (PIPEDA), Australia (Privacy Act), and other jurisdictions have analogous rights. Contact us and we will honour them.

---

## 7. Data retention

- Local data is retained for as long as the app is installed on your device.
- iCloud data follows Apple's retention rules for your personal iCloud storage.
- We (the developer) retain nothing on our servers because we operate none.

---

## 8. Children's privacy

GymTrack Pro is rated 4+ on the App Store but is designed for an adult audience interested in strength training. It is not directed at children under 13. We do not knowingly collect information from children under 13. If a parent or guardian believes a child under 13 has used the app and you want the data removed from that device, simply uninstall the app.

---

## 9. Security

We take the security of your data seriously:

- Local data is protected by iOS Data Protection (class `NSFileProtectionComplete` for sensitive fields).
- iCloud sync uses Apple's TLS transport and at-rest encryption.
- The app contains no custom cryptography — we rely on Apple's vetted encryption implementations.
- The app contains no third-party SDKs, reducing supply-chain risk.
- We do not store, transmit, or process passwords, authentication tokens (beyond your system iCloud token, which we never see), or payment information.

No security measure is perfect. You can reduce risk by keeping your iOS version up to date and using a strong device passcode plus Face ID or Touch ID.

---

## 10. International transfers

Your data does not leave your device unless you opt into iCloud sync. If you do, Apple may store it in data centres in various countries as part of their global iCloud infrastructure. Apple's transfers are governed by [Apple's Privacy Policy](https://www.apple.com/legal/privacy/en-ww/) and Standard Contractual Clauses where applicable.

---

## 11. Changes to this policy

We may update this Privacy Policy from time to time, for example if we add new features. When we do:

- The "Last updated" date at the top of this document will change.
- Material changes will be communicated via an in-app notice on first launch after the update.
- Continued use of the app after an update constitutes acceptance of the revised policy, but you may always uninstall if you disagree.

We will not make a change that retroactively broadens our use of data you already provided without giving you a clear opt-in opportunity.

---

## 12. Contact

If you have questions, concerns, or requests regarding this Privacy Policy or your data:

**D. Raj Gurung**
Email: [divy5831@gmail.com](mailto:divy5831@gmail.com)
GitHub: [github.com/D-Raj-Grg/gymtrackpromax](https://github.com/D-Raj-Grg/gymtrackpromax)

Please include "GymTrack Pro — Privacy" in the subject line. We aim to respond within 14 days.

---

*This policy was drafted specifically for GymTrack Pro based on the app's actual data practices as of the effective date above. It is provided for your understanding and for App Store / TestFlight compliance. It is not legal advice.*

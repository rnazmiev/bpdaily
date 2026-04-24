---
title: Privacy Policy
layout: default
permalink: /privacy/
---

# BP Daily — Privacy Policy

**Last updated:** 2026-04-23

This Privacy Policy describes how **BP Daily** ("the App", "we", "us") handles your information. BP Daily is a senior-friendly blood-pressure and pulse tracking application developed by **Rushan Nazmiev** and published on Google Play.

Contact for privacy matters: **nazmievjob@gmail.com**

## 1. TL;DR

BP Daily is an **offline-first** application. Every blood-pressure reading, pulse measurement, reminder, and note you enter stays on your device. We do not operate servers that receive your health data, we do not sell or share your data, and we do not include any analytics, advertising, or third-party tracking SDKs in the App.

## 2. Data the App uses

### 2.1 Data you enter and keep on your device

The following is stored locally on your phone and never sent off-device:

- Blood-pressure readings (systolic, diastolic, pulse, optional note)
- Pulse measurements taken via the camera (PPG)
- Timestamps associated with those readings
- Reminder schedules you create
- App preferences (units, onboarding state, daily usage counters for the free tier)

Storage is implemented with a local SQLite database (via the `drift` package) and `SharedPreferences`, both sandboxed to the App on your device.

### 2.2 Pseudonymous local identifier

When you first open the App, a random UUID is generated and stored in the Android Keystore (via `flutter_secure_storage`). This identifier is **reserved** for an optional cloud-sync feature that is **not currently enabled**. It does not leave your device today, and it is not linked to your name, email, Google account, or any other personal identifier.

### 2.3 Camera and PPG

When you tap "Measure Pulse", the App briefly activates the back camera and flash to estimate your heart rate by measuring red-channel brightness changes at your fingertip. **No image, video, or frame is saved, uploaded, or retained.** Only a numeric brightness sample per frame is processed in memory and discarded immediately after processing.

The App **does not** measure or claim to measure blood pressure via the camera — only pulse, in line with FTC guidance for PPG-based wellness features.

### 2.4 Notifications

If you create reminders, the App schedules them through the device's local notification system. No push-notification server is involved, and no data is transmitted.

## 3. Data we do NOT collect

We do not collect, store, or transmit:

- Analytics, crash reports, or usage telemetry
- Advertising identifiers
- Location data
- Contacts, photos library, microphone audio
- Your name, email address, phone number, or payment information (see §4)

## 4. Subscriptions and payment

BP Daily offers an optional premium subscription, **BP Daily Pro**, billed through Google Play.

- **All payments are processed by Google.** We never see or store your card number, billing address, or Google account details.
- The App receives from Google a signed token that indicates whether your subscription is active. That token is cached locally on your device for offline access.
- Refunds, cancellations, and renewals are governed by Google Play's policies: [https://support.google.com/googleplay/answer/7018481](https://support.google.com/googleplay/answer/7018481)

## 5. Permissions the App requests

| Permission | Why |
|---|---|
| Camera | Only to measure your pulse (PPG). |
| Notifications | To deliver the reminders you schedule. |
| Internet | To verify your subscription status with Google Play. Reserved for optional future cloud-sync. |
| Boot completed / wake lock | To re-arm scheduled reminders after a device reboot. |

We do not request location, contacts, photos, microphone, or any identifier-related permissions.

## 6. Third parties

The only third party the App communicates with is **Google Play Billing**, and only to verify your subscription status. See Google's privacy practices: [https://policies.google.com/privacy](https://policies.google.com/privacy).

We do **not** integrate Firebase Analytics, Google Analytics, Crashlytics, Sentry, Facebook SDK, or any advertising or tracking network.

## 7. Children

BP Daily is intended for adults monitoring their own blood pressure. We do not knowingly target or process data from children under 13 (or under 16 where required by law).

## 8. Data retention and deletion

Your readings and settings remain on your device until **you** delete them. You can:

- **Delete a single reading** — tap a row in History → Delete.
- **Delete all data** — uninstall the App. All local data is removed by Android.

Because we do not store your data on any server, there is no server-side copy to delete.

## 9. Your rights (GDPR / UK GDPR / CCPA)

Since all your personal and health data stays on your device and is never transmitted to us, we do not hold a copy that you would need to request, export, correct, or delete from us. You have full control over your data directly in the App.

If you believe we are nonetheless processing your personal data on our servers (we are not), or have any question or complaint about this Policy, contact us at **nazmievjob@gmail.com**. We respond within 30 days.

EU residents have the right to lodge a complaint with their local data protection authority.

California residents: we do not sell or share personal information as defined by the CCPA.

## 10. Security

All data is stored in the App's sandboxed storage on your device. The pseudonymous local identifier is stored in the Android Keystore. We rely on Android's system-level encryption (enabled by default on Android 10+) to protect data at rest.

No transmission over the internet is ever 100% secure; however, because the App does not transmit your health data, this concern is limited to the subscription-verification channel between your device and Google Play, which is secured by Google.

## 11. Changes to this Policy

If we update how the App handles data, we will revise this Policy and change the "Last updated" date at the top. Material changes will be announced in the App before taking effect.

## 12. Contact

Developer: **Rushan Nazmiev**
Email: **nazmievjob@gmail.com**

If you prefer to reach us about something specific to privacy, use the same email with "Privacy" in the subject line.

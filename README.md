# Blin Agent for Android

> **Quick-testing beta — not a production release.** This is the `1.0` debug APK for short, experimental testing. It has not been independently security-audited, and behavior may change or fail.

Blin Agent is an experimental Android AI assistant. Its current build combines chat with screen-aware task automation. The APK metadata identifies package `com.wod.blinagent`, version `1.0` (version code `1`), and an Android minimum SDK of 23.

## Download and test

Download **`BlinAgent-debug.apk`** from the [latest release](../../releases/latest). Install it only on a device you control and trust. Android may ask you to allow installation from that download source. For screen automation, Android also requires you to enable the Blin Agent Accessibility service in Settings; read the security notes below before granting it.

This is a debug build, not an app-store release. Prefer a spare test device or a test profile with no personal, financial, or confidential data. Uninstall it or revoke its permissions when you finish testing.

## What it can do

Based on the packaged Android code and manifest, Blin Agent appears designed to:

- chat with an AI assistant and route requests to provider services, including Groq, Google Generative Language, OpenRouter, Cloudflare, and a Firebase backend;
- accept voice input and image attachments for assistant requests;
- use Android's Accessibility service to inspect on-screen context and carry out screen interactions such as tapping, typing, and navigating between app screens;
- run a floating overlay/service for agent controls and ongoing tasks.

These capabilities were identified by static inspection of the APK. The app was not run in an Android emulator or on a device as part of preparing this release, so the feature list is not a runtime test or a security audit.

## Free-tier keys and production credentials

This quick-test APK intentionally retains the bundled **free-tier testing API keys**, as requested by the maintainer. API keys inside an APK are extractable: anyone who downloads it can copy and use them, and their free quotas may be exhausted or the keys may be revoked. They are for brief testing only—not for production, private use, or a service that needs reliable availability. The maintainer should revoke or rotate them when the public test ends.

The maintainer says paid production keys will be kept server-side in **Cloudflare Workers**, not shipped in the client APK. This release does not claim that server-side setup has been independently verified.

## Permissions and privacy

The manifest requests internet and network access, microphone access, overlay display, installed-package visibility, foreground-service operation, wake lock, and alarm scheduling. The app also declares an Accessibility service. If enabled, that service can read what is displayed and perform actions in other apps. Use it only on a device you control, and do not use Blin Agent with banking, password, health, work, or other sensitive apps or information.

Depending on the task and provider, prompts, images, and on-screen context may be sent to online AI services or the app's Firebase backend. Do not enter secrets or confidential information. Review provider privacy and retention practices before testing.

## Feedback and collaboration

Testing feedback and collaboration are welcome. Open an issue with the Android version, device model, steps to reproduce, and expected versus actual behavior. Remove personal information, screenshots of private content, and API keys from reports. See [`SECURITY.md`](SECURITY.md) for handling security concerns.

## Project notes

- This repository distributes the APK release asset; Android source code is not included.
- The build is labelled `debug`; signing identity and install/update compatibility have not been independently verified.
- No reuse license has been selected yet. Public download does not by itself grant permission to redistribute or modify the app.

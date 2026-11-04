## Quick-testing beta only

This `1.0` debug APK is shared for brief evaluation and feedback. It is experimental, has not been independently security-audited, and is not suitable for production or sensitive devices/accounts.

## What it can do

Blin Agent is an Android AI assistant with chat, voice input, and image attachments. The build appears designed to use Android Accessibility to inspect screen context and automate actions such as taps, text entry, and navigation. It also includes a floating control/service. These capabilities are based on static APK inspection; they have not been runtime-tested for this release.

## Free-tier test keys

This APK intentionally includes free-tier API keys for quick testing, as directed by the maintainer. Because the keys are bundled in an Android client, they can be extracted, copied, used by others, rate-limited, exhausted, or revoked. They are not production credentials. The maintainer says paid production keys will be kept server-side in Cloudflare Workers and not in the Android client. Rotate or revoke the test keys when public testing ends.

## Permissions and safety

The APK requests network access, microphone access, overlay display, installed-package visibility, foreground-service operation, wake lock, and alarm scheduling. It also declares an Accessibility service. Enabling Accessibility can let the agent read visible screen content and act in other apps. Install only on a device/profile you control, and do not use it with banking, password, health, work, or other sensitive apps.

Depending on the request, prompts, images, and screen context may be sent to online AI providers or the app's Firebase backend. Do not enter secrets or confidential information.

## Install and report feedback

Download `BlinAgent-debug.apk` below and sideload it on a compatible Android device. Android may require permission to install from that download source. Enable Accessibility only if you understand and accept the access it grants. Report bugs through the repository's Issues tab; remove personal information and credentials from reports.

## Artifact integrity

- App label: Blin Agent
- Package: `com.wod.blinagent`
- Version: `1.0` (version code `1`)
- Asset: `BlinAgent-debug.apk`
- SHA-256: `98998604669a1a146c48688a4354b8cad98ca45679a56751ccb0eab8cef1ba99`

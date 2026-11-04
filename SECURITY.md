# Security notes

Blin Agent is an experimental quick-testing beta, not a security-reviewed production app.

- Do not use it with sensitive accounts or confidential information.
- The public beta APK includes free-tier API keys at the maintainer's direction. They are extractable and may be copied or exhaust their quotas. The maintainer should rotate or revoke them after the testing period.
- Paid production keys are intended to remain server-side in Cloudflare Workers; do not add them to the Android client.
- Enabling the Accessibility service allows the app to inspect screen content and act in other apps. Only enable it on a test device/profile that you control.
- Do not post API keys, private data, or exploitable vulnerability details in public issues. Contact the maintainer through their GitHub profile to arrange a private disclosure channel.

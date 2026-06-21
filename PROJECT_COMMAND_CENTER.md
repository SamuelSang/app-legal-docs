# Project Command Center

Repo: `SamuelSang/app-legal-docs`
Role: shared privacy policy / legal docs for App releases.

## Hard rules

- Do not make legal/privacy claims that are stronger than actual app behavior.
- Do not reuse one privacy policy across apps if data collection, IAP, analytics, health/psychology, or account behavior differs.
- Keep public URLs stable after App Store submission.
- Every App Store privacy answer must match the policy text.

## PR review checklist

P0:
- Privacy policy URL breaks.
- Policy contradicts app behavior or App Store privacy answers.
- Sensitive categories are misstated: health, psychology, location, identifiers, diagnostics, analytics, payment.

P1:
- App-specific policy differences are collapsed into generic text.
- Effective date/version not updated when material policy text changes.

P2:
- Ambiguous wording, missing contact path, weak formatting, or outdated app name.

## Release gate

Before submitting any App:

- Correct policy URL is reachable in browser.
- App name, Bundle ID, data categories, analytics, payments, and contact info match the submitted build.
- Screenshot/metadata claims do not imply undeclared data use.
- This repo is referenced from the app repo's `PROJECT_COMMAND_CENTER.md` if it is part of that release.

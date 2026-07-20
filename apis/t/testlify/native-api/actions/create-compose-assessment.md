# Create Compose Assessment with Testlify

Creates a custom assessment in Testlify from scratch.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/assessment/compose`
- **Base URL:** `https://api.testlify.com`
- **Official documentation:** [Create Compose Assessment](https://docs.testlify.com/reference/create_compose_assessment)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `title` | body | `string` | yes |
| `testLibraryIds[]` | body | `array<string>` | yes |
| `settings.extraTime` | body | `number` | no |
| `settings.feedbackRating` | body | `number` | no |
| `settings.feedbackRemark` | body | `string` | no |
| `settings.verifyPassword` | body | `string` | no |
| `settings.welcomeVideoUploadUrl` | body | `string` | no |
| `settings.welcomeVideoKey` | body | `string` | no |
| `settings.welcomeVideoPath` | body | `string` | no |
| `settings.externalWelcomeVideoLink` | body | `string` | no |
| `settings.autoPlayWelcomeVideo` | body | `boolean` | no |
| `settings.titleSlug` | body | `string` | no |
| `settings.attemptTestLibrariesRequired` | body | `boolean` | no |
| `settings.webcamAndMicrophoneAccessRequired` | body | `boolean` | no |
| `settings.snapshotCaptureRequired` | body | `boolean` | no |
| `settings.snapshotIntervalType` | body | `string` | no |
| `settings.customSnapshotInterval` | body | `number` | no |
| `settings.defaultLanguage` | body | `string` | no |
| `settings.supportedLanguages[]` | body | `array<string>` | no |
| `settings.skipRegistration` | body | `boolean` | no |
| `settings.enableFeedbackAfterSection` | body | `boolean` | no |
| `settings.enableFeedback` | body | `boolean` | no |

# Create Android App with Firebase

Creates an Android app in Firebase.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1beta1/projects/[:projectId]/androidApps`
- **Base URL:** `https://firebase.googleapis.com`
- **Official documentation:** [Create Android App](https://firebase.google.com/docs/reference/firebase-management/rest/v1beta1/projects.androidApps/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | Firebase project ID. |
| `packageName` | body | `string` | yes | Canonical package name of the Android app. |
| `displayName` | body | `string` | no | User-assigned display name for the Android app. |
| `apiKeyId` | body | `string` | no | Google-assigned UID for the Firebase API key associated with the Android app. |
| `sha1Hashes[]` | body | `array<string>` | no | SHA-1 certificate hashes for the Android app. |
| `sha256Hashes[]` | body | `array<string>` | no | SHA-256 certificate hashes for the Android app. |

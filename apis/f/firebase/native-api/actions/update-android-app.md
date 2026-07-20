# Update Android App with Firebase

Updates an existing Android app in Firebase.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1beta1/projects/[:projectId]/androidApps/[:appId]`
- **Base URL:** `https://firebase.googleapis.com`
- **Official documentation:** [Update Android App](https://firebase.google.com/docs/reference/firebase-management/rest/v1beta1/projects.androidApps/patch)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | Firebase project ID. |
| `appId` | path | `string` | yes | Firebase Android app ID. |
| `updateMask` | query | `string` | no | Comma-separated field mask specifying which Android app fields to update. |
| `displayName` | body | `string` | no | User-assigned display name for the Android app. |
| `apiKeyId` | body | `string` | no | Google-assigned UID for the Firebase API key associated with the Android app. |
| `etag` | body | `string` | no | Checksum sent with update requests to avoid overwriting a stale Android app resource. |

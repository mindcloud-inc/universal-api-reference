# Update Web App with Firebase

Updates an existing web app in Firebase.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1beta1/projects/[:projectId]/webApps/[:appId]`
- **Base URL:** `https://firebase.googleapis.com`
- **Official documentation:** [Update Web App](https://firebase.google.com/docs/reference/firebase-management/rest/v1beta1/projects.webApps/patch)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | Firebase project ID. |
| `appId` | path | `string` | yes | Firebase Web app ID. |
| `updateMask` | query | `string` | no | Comma-separated field mask specifying which web app fields to update. |
| `displayName` | body | `string` | no | User-assigned display name for the web app. |
| `apiKeyId` | body | `string` | no | Google-assigned UID for the Firebase API key associated with the web app. |
| `appUrls[]` | body | `array<string>` | no | URLs where the web app is hosted. |
| `etag` | body | `string` | no | Checksum sent with update requests to avoid overwriting a stale web app resource. |

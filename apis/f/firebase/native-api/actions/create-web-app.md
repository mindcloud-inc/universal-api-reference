# Create Web App with Firebase

Creates a web app in Firebase.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1beta1/projects/[:projectId]/webApps`
- **Base URL:** `https://firebase.googleapis.com`
- **Official documentation:** [Create Web App](https://firebase.google.com/docs/reference/firebase-management/rest/v1beta1/projects.webApps/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | Firebase project ID. |
| `displayName` | body | `string` | yes | User-assigned display name for the web app. |
| `apiKeyId` | body | `string` | no | Google-assigned UID for the Firebase API key associated with the web app. |
| `appUrls[]` | body | `array<string>` | no | URLs where the web app is hosted. |

# Update iOS App with Firebase

Updates an existing iOS app in Firebase.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1beta1/projects/[:projectId]/iosApps/[:appId]`
- **Base URL:** `https://firebase.googleapis.com`
- **Official documentation:** [Update iOS App](https://firebase.google.com/docs/reference/firebase-management/rest/v1beta1/projects.iosApps/patch)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | Firebase project ID. |
| `appId` | path | `string` | yes | Firebase iOS app ID. |
| `updateMask` | query | `string` | no | Comma-separated field mask specifying which iOS app fields to update. |
| `displayName` | body | `string` | no | User-assigned display name for the iOS app. |
| `apiKeyId` | body | `string` | no | Google-assigned UID for the Firebase API key associated with the iOS app. |
| `appStoreId` | body | `string` | no | Apple ID assigned to the iOS app by the App Store. |
| `teamId` | body | `string` | no | Apple Developer Team ID associated with the app. |
| `etag` | body | `string` | no | Checksum sent with update requests to avoid overwriting a stale iOS app resource. |

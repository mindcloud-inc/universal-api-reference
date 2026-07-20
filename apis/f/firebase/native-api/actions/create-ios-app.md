# Create iOS App with Firebase

Creates an iOS app in Firebase.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1beta1/projects/[:projectId]/iosApps`
- **Base URL:** `https://firebase.googleapis.com`
- **Official documentation:** [Create iOS App](https://firebase.google.com/docs/reference/firebase-management/rest/v1beta1/projects.iosApps/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | Firebase project ID. |
| `bundleId` | body | `string` | yes | Canonical bundle ID of the iOS app. |
| `displayName` | body | `string` | no | User-assigned display name for the iOS app. |
| `apiKeyId` | body | `string` | no | Google-assigned UID for the Firebase API key associated with the iOS app. |
| `appStoreId` | body | `string` | no | Apple ID assigned to the iOS app by the App Store. |
| `teamId` | body | `string` | no | Apple Developer Team ID associated with the app. |

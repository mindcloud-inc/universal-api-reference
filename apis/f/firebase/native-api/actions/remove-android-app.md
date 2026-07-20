# Remove Android App with Firebase

Removes an Android app from Firebase.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1beta1/projects/[:projectId]/androidApps/[:appId]:remove`
- **Base URL:** `https://firebase.googleapis.com`
- **Official documentation:** [Remove Android App](https://firebase.google.com/docs/reference/firebase-management/rest/v1beta1/projects.androidApps/remove)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | Firebase project ID. |
| `appId` | path | `string` | yes | Firebase Android app ID. |
| `allowMissing` | body | `boolean` | no | Allow the request to succeed when the app is already absent. |
| `validateOnly` | body | `boolean` | no | Validate the request without removing the Android app. |
| `immediate` | body | `boolean` | no | Remove the app immediately instead of allowing the normal expiration window. |
| `etag` | body | `string` | no | Checksum used to avoid removing a stale Android app resource. |

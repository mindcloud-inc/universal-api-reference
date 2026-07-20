# Undelete iOS App with Firebase

Restores a removed iOS app in Firebase.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1beta1/projects/[:projectId]/iosApps/[:appId]:undelete`
- **Base URL:** `https://firebase.googleapis.com`
- **Official documentation:** [Undelete iOS App](https://firebase.google.com/docs/reference/firebase-management/rest/v1beta1/projects.iosApps/undelete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | Firebase project ID. |
| `appId` | path | `string` | yes | Firebase iOS app ID. |
| `validateOnly` | body | `boolean` | no | Validate the request without restoring the iOS app. |
| `etag` | body | `string` | no | Checksum used to avoid restoring a stale iOS app resource. |

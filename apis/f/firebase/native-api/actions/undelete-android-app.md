# Undelete Android App with Firebase

Restores a removed Android app in Firebase.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1beta1/projects/[:projectId]/androidApps/[:appId]:undelete`
- **Base URL:** `https://firebase.googleapis.com`
- **Official documentation:** [Undelete Android App](https://firebase.google.com/docs/reference/firebase-management/rest/v1beta1/projects.androidApps/undelete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | Firebase project ID. |
| `appId` | path | `string` | yes | Firebase Android app ID. |
| `validateOnly` | body | `boolean` | no | Validate the request without restoring the Android app. |
| `etag` | body | `string` | no | Checksum used to avoid restoring a stale Android app resource. |

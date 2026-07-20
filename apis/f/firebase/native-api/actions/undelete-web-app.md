# Undelete Web App with Firebase

Restores a removed web app in Firebase.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1beta1/projects/[:projectId]/webApps/[:appId]:undelete`
- **Base URL:** `https://firebase.googleapis.com`
- **Official documentation:** [Undelete Web App](https://firebase.google.com/docs/reference/firebase-management/rest/v1beta1/projects.webApps/undelete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | Firebase project ID. |
| `appId` | path | `string` | yes | Firebase Web app ID. |
| `validateOnly` | body | `boolean` | no | Validate the request without restoring the web app. |
| `etag` | body | `string` | no | Checksum used to avoid restoring a stale web app resource. |

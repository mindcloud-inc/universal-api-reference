# Remove Web App with Firebase

Removes a web app from Firebase.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1beta1/projects/[:projectId]/webApps/[:appId]:remove`
- **Base URL:** `https://firebase.googleapis.com`
- **Official documentation:** [Remove Web App](https://firebase.google.com/docs/reference/firebase-management/rest/v1beta1/projects.webApps/remove)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | Firebase project ID. |
| `appId` | path | `string` | yes | Firebase Web app ID. |
| `allowMissing` | body | `boolean` | no | Allow the request to succeed when the app is already absent. |
| `validateOnly` | body | `boolean` | no | Validate the request without removing the web app. |
| `immediate` | body | `boolean` | no | Remove the app immediately instead of allowing the normal expiration window. |
| `etag` | body | `string` | no | Checksum used to avoid removing a stale web app resource. |

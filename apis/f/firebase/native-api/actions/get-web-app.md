# Get Web App with Firebase

Retrieves a web app from Firebase.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1beta1/projects/[:projectId]/webApps/[:appId]`
- **Base URL:** `https://firebase.googleapis.com`
- **Official documentation:** [Get Web App](https://firebase.google.com/docs/reference/firebase-management/rest/v1beta1/projects.webApps/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | Firebase project ID. |
| `appId` | path | `string` | yes | Firebase Web app ID. |

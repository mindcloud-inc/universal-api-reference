# Get Android App with Firebase

Retrieves an Android app from Firebase.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1beta1/projects/[:projectId]/androidApps/[:appId]`
- **Base URL:** `https://firebase.googleapis.com`
- **Official documentation:** [Get Android App](https://firebase.google.com/docs/reference/firebase-management/rest/v1beta1/projects.androidApps/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | Firebase project ID. |
| `appId` | path | `string` | yes | Firebase Android app ID. |

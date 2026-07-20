# Get iOS App with Firebase

Retrieves an iOS app from Firebase.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1beta1/projects/[:projectId]/iosApps/[:appId]`
- **Base URL:** `https://firebase.googleapis.com`
- **Official documentation:** [Get iOS App](https://firebase.google.com/docs/reference/firebase-management/rest/v1beta1/projects.iosApps/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | Firebase project ID. |
| `appId` | path | `string` | yes | Firebase iOS app ID. |

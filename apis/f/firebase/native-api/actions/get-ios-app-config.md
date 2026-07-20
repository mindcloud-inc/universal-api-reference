# Get iOS App Config with Firebase

Retrieves iOS app config from Firebase.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1beta1/projects/[:projectId]/iosApps/[:appId]/config`
- **Base URL:** `https://firebase.googleapis.com`
- **Official documentation:** [Get iOS App Config](https://firebase.google.com/docs/reference/firebase-management/rest/v1beta1/projects.iosApps/getConfig)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | Firebase project ID. |
| `appId` | path | `string` | yes | Firebase iOS app ID. |

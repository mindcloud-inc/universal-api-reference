# Get Android App Config with Firebase

Retrieves Android app config from Firebase.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1beta1/projects/[:projectId]/androidApps/[:appId]/config`
- **Base URL:** `https://firebase.googleapis.com`
- **Official documentation:** [Get Android App Config](https://firebase.google.com/docs/reference/firebase-management/rest/v1beta1/projects.androidApps/getConfig)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | Firebase project ID. |
| `appId` | path | `string` | yes | Firebase Android app ID. |

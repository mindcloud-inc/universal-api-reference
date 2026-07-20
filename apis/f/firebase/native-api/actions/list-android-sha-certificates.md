# List Android SHA Certificates with Firebase

Retrieves Android SHA certificates from Firebase.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1beta1/projects/[:projectId]/androidApps/[:appId]/sha`
- **Base URL:** `https://firebase.googleapis.com`
- **Official documentation:** [List Android SHA Certificates](https://firebase.google.com/docs/reference/firebase-management/rest/v1beta1/projects.androidApps.sha/list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | Firebase project ID. |
| `appId` | path | `string` | yes | Firebase Android app ID. |

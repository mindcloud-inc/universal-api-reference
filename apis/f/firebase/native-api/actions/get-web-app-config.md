# Get Web App Config with Firebase

Retrieves web app config from Firebase.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1beta1/projects/[:projectId]/webApps/[:appId]/config`
- **Base URL:** `https://firebase.googleapis.com`
- **Official documentation:** [Get Web App Config](https://firebase.google.com/docs/reference/firebase-management/rest/v1beta1/projects.webApps/getConfig)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | Firebase project ID. |
| `appId` | path | `string` | yes | Firebase Web app ID. |

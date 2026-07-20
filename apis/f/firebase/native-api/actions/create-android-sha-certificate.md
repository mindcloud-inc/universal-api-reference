# Create Android SHA Certificate with Firebase

Creates an Android SHA certificate in Firebase.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1beta1/projects/[:projectId]/androidApps/[:appId]/sha`
- **Base URL:** `https://firebase.googleapis.com`
- **Official documentation:** [Create Android SHA Certificate](https://firebase.google.com/docs/reference/firebase-management/rest/v1beta1/projects.androidApps.sha/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | Firebase project ID. |
| `appId` | path | `string` | yes | Firebase Android app ID. |
| `certType` | body | `string` | yes | Type of SHA certificate encoded in the hash. |
| `shaHash` | body | `string` | yes | Certificate hash for the Android app. |

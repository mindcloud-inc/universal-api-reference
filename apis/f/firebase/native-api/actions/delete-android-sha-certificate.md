# Delete Android SHA Certificate with Firebase

Deletes an Android SHA certificate from Firebase.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v1beta1/projects/[:projectId]/androidApps/[:appId]/sha/[:shaHash]`
- **Base URL:** `https://firebase.googleapis.com`
- **Official documentation:** [Delete Android SHA Certificate](https://firebase.google.com/docs/reference/firebase-management/rest/v1beta1/projects.androidApps.sha/delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | Firebase project ID. |
| `appId` | path | `string` | yes | Firebase Android app ID. |
| `shaHash` | path | `string` | yes | SHA certificate hash. |

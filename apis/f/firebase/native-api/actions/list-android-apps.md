# List Android Apps with Firebase

Retrieves Android apps from Firebase.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1beta1/projects/[:projectId]/androidApps`
- **Base URL:** `https://firebase.googleapis.com`
- **Official documentation:** [List Android Apps](https://firebase.google.com/docs/reference/firebase-management/rest/v1beta1/projects.androidApps/list)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | Firebase project ID. |
| `showDeleted` | query | `string` | no | Whether deleted Android apps should be included in results. |

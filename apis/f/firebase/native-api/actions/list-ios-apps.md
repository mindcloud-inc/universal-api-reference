# List iOS Apps with Firebase

Retrieves iOS apps from Firebase.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1beta1/projects/[:projectId]/iosApps`
- **Base URL:** `https://firebase.googleapis.com`
- **Official documentation:** [List iOS Apps](https://firebase.google.com/docs/reference/firebase-management/rest/v1beta1/projects.iosApps/list)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | Firebase project ID. |
| `showDeleted` | query | `string` | no | Whether deleted iOS apps should be included in results. |

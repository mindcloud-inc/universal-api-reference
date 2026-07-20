# List Web Apps with Firebase

Retrieves web apps from Firebase.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1beta1/projects/[:projectId]/webApps`
- **Base URL:** `https://firebase.googleapis.com`
- **Official documentation:** [List Web Apps](https://firebase.google.com/docs/reference/firebase-management/rest/v1beta1/projects.webApps/list)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | Firebase project ID. |
| `showDeleted` | query | `string` | no | Whether deleted web apps should be included in results. |

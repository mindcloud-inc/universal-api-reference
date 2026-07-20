# Search Project Apps with Firebase

Finds apps in a Firebase project.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1beta1/projects/[:projectId]:searchApps`
- **Base URL:** `https://firebase.googleapis.com`
- **Official documentation:** [Search Project Apps](https://firebase.google.com/docs/reference/firebase-management/rest/v1beta1/projects/searchApps)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | Firebase project ID. |
| `filter` | query | `string` | no | Firebase app search filter. |
| `showDeleted` | query | `boolean` | no | Whether deleted apps should be included in results. |

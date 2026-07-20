# Delete Project User Tag with Openlayer

Deletes a project user tag from Openlayer.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/projects/:projectId/user-tags/:tagId`
- **Base URL:** `https://api.openlayer.com/v1`
- **Official documentation:** [Delete Project User Tag](https://api.openlayer.com/v1/openapi.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | The Openlayer project ID. |
| `tagId` | path | `string` | yes | The user tag ID. |

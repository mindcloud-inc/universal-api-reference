# Update Project User Tag with Openlayer

Updates an existing project user tag in Openlayer.

## Endpoint

- **Method:** `PUT`
- **Path:** `/projects/:projectId/user-tags/:tagId`
- **Base URL:** `https://api.openlayer.com/v1`
- **Official documentation:** [Update Project User Tag](https://api.openlayer.com/v1/openapi.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `color` | body | `string` | no | Updated tag color. |
| `name` | body | `string` | no | Updated tag name. |
| `projectId` | path | `string` | yes | The Openlayer project ID. |
| `tagId` | path | `string` | yes | The user tag ID. |

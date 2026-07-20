# Delete Workspace Property with Blaze AI

Deletes an existing workspace property from Blaze AI.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/v1/w/:workspace_id/properties/:id`
- **Base URL:** `https://api.blaze.ai`
- **Official documentation:** [Delete Workspace Property](https://api.blaze.ai/api/documentation#!/properties/deleteApiV1WWorkspaceIdPropertiesId)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspace_id` | path | `number` | yes |
| `id` | path | `number` | yes |

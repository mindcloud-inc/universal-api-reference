# Remove Doc Property with Blaze AI

Deletes an existing document property from Blaze AI.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/v1/w/:workspace_id/docs/:doc_id/properties/:id`
- **Base URL:** `https://api.blaze.ai`
- **Official documentation:** [Remove Doc Property](https://api.blaze.ai/api/documentation#!/properties/deleteApiV1WWorkspaceIdDocsDocIdPropertiesId)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspace_id` | path | `number` | yes |
| `doc_id` | path | `number` | yes |
| `id` | path | `number` | yes |

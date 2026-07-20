# Delete Handbook Item with Blaze AI

Deletes an existing handbook item from Blaze AI.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/v1/w/:workspace_id/handbooks/:handbook_id/items/:id`
- **Base URL:** `https://api.blaze.ai`
- **Official documentation:** [Delete Handbook Item](https://api.blaze.ai/api/documentation#!/handbook%20items/deleteApiV1WWorkspaceIdHandbooksHandbookIdItemsId)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspace_id` | path | `number` | yes |
| `handbook_id` | path | `number` | yes |
| `id` | path | `number` | yes |

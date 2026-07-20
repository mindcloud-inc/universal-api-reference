# Update Folder with Blaze AI

Updates an existing folder in Blaze AI.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v1/w/:workspace_id/folders/:id`
- **Base URL:** `https://api.blaze.ai`
- **Official documentation:** [Update Folder](https://api.blaze.ai/api/documentation#!/folders/patchApiV1WWorkspaceIdFoldersId)

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
| `folder[title]` | body | `string` | yes |

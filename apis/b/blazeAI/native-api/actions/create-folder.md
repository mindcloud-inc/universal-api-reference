# Create Folder with Blaze AI

Creates a new folder in Blaze AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/w/:workspace_id/folders`
- **Base URL:** `https://api.blaze.ai`
- **Official documentation:** [Create Folder](https://api.blaze.ai/api/documentation#!/folders/postApiV1WWorkspaceIdFolders)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspace_id` | path | `number` | yes |
| `folder[title]` | body | `string` | yes |
| `folder[parent_folder_id]` | body | `string` | no |

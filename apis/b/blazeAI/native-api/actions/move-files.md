# Move Files with Blaze AI

Moves files between folders in Blaze AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/w/:workspace_id/files/move`
- **Base URL:** `https://api.blaze.ai`
- **Official documentation:** [Move Files](https://api.blaze.ai/api/documentation#!/files/postApiV1WWorkspaceIdFilesMove)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspace_id` | path | `number` | yes |
| `folder_ids` | body | `string` | no |
| `doc_ids` | body | `string` | no |
| `destination_folder_id` | body | `number` | no |
| `destination_workspace_id` | body | `number` | no |

# List Folders with Blaze AI

Retrieves folders from a Blaze AI workspace.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/w/:workspace_id/folders`
- **Base URL:** `https://api.blaze.ai`
- **Official documentation:** [List Folders](https://api.blaze.ai/api/documentation#!/folders/getApiV1WWorkspaceIdFolders)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspace_id` | path | `number` | yes |
| `parent_folder_id` | query | `string` | no |

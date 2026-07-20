# List Folder Children with Frame.io v4

Retrieves child items for a folder in Frame.io v4.

## Endpoint

- **Method:** `GET`
- **Path:** `/accounts/:accountId/folders/:folderId/children`
- **Base URL:** `https://api.frame.io/v4`
- **Official documentation:** [List Folder Children](https://next.developer.frame.io/platform/api-reference/folders/index)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `account_id` | path | `string` | yes |
| `folder_id` | path | `string` | yes |
| `include` | query | `string` | no |
| `type` | query | `string` | no |

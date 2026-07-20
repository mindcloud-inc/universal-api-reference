# List Files with Frame.io v4

Retrieves files from a folder in Frame.io v4.

## Endpoint

- **Method:** `GET`
- **Path:** `/accounts/:accountId/folders/:folderId/files`
- **Base URL:** `https://api.frame.io/v4`
- **Official documentation:** [List Files](https://next.developer.frame.io/platform/api-reference/files/list)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `account_id` | path | `string` | yes |
| `folder_id` | path | `string` | yes |
| `include` | query | `string` | no |

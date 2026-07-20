# Get Folder with Frame.io v4

Retrieves a folder from Frame.io v4.

## Endpoint

- **Method:** `GET`
- **Path:** `/accounts/:accountId/folders/:folderId`
- **Base URL:** `https://api.frame.io/v4`
- **Official documentation:** [Get Folder](https://next.developer.frame.io/platform/api-reference/folders/show)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `account_id` | path | `string` | yes |
| `folder_id` | path | `string` | yes |
| `include` | query | `string` | no |

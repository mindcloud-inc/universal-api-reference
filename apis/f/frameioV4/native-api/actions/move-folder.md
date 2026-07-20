# Move Folder with Frame.io v4

Moves a folder in Frame.io v4.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/accounts/:accountId/folders/:folderId/move`
- **Base URL:** `https://api.frame.io/v4`
- **Official documentation:** [Move Folder](https://next.developer.frame.io/platform/api-reference/folders/move)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `account_id` | path | `string` | yes |
| `folder_id` | path | `string` | yes |
| `data` | body | `object` | yes |

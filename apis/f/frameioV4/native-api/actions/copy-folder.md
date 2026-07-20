# Copy Folder with Frame.io v4

Copies a folder in Frame.io v4.

## Endpoint

- **Method:** `POST`
- **Path:** `/accounts/:accountId/folders/:folderId/copy`
- **Base URL:** `https://api.frame.io/v4`
- **Official documentation:** [Copy Folder](https://next.developer.frame.io/platform/api-reference/folders/copy)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `account_id` | path | `string` | yes |
| `folder_id` | path | `string` | yes |
| `copy_metadata` | query | `boolean` | no |
| `data` | body | `object` | no |

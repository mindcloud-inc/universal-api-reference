# Create Folder with Frame.io v4

Creates a new subfolder in Frame.io v4.

## Endpoint

- **Method:** `POST`
- **Path:** `/accounts/:accountId/folders/:folderId/folders`
- **Base URL:** `https://api.frame.io/v4`
- **Official documentation:** [Create Folder](https://next.developer.frame.io/platform/api-reference/folders/create)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `account_id` | path | `string` | yes |
| `folder_id` | path | `string` | yes |
| `data` | body | `object` | yes |

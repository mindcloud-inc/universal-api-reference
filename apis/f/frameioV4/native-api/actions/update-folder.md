# Update Folder with Frame.io v4

Updates an existing folder in Frame.io v4.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/accounts/:accountId/folders/:folderId`
- **Base URL:** `https://api.frame.io/v4`
- **Official documentation:** [Update Folder](https://next.developer.frame.io/platform/api-reference/folders/update)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `account_id` | path | `string` | yes |
| `folder_id` | path | `string` | yes |
| `data` | body | `object` | yes |

# Create File Local Upload with Frame.io v4

Creates a new file via local upload in Frame.io v4.

## Endpoint

- **Method:** `POST`
- **Path:** `/accounts/:accountId/folders/:folderId/files/local_upload`
- **Base URL:** `https://api.frame.io/v4`
- **Official documentation:** [Create File Local Upload](https://next.developer.frame.io/platform/api-reference/files/create-local-upload)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `account_id` | path | `string` | yes |
| `folder_id` | path | `string` | yes |
| `data` | body | `object` | yes |

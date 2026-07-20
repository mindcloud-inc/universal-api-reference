# Import File with Frame.io v4

Imports a file into Frame.io v4.

## Endpoint

- **Method:** `POST`
- **Path:** `/accounts/:accountId/folders/:folderId/files/import`
- **Base URL:** `https://api.frame.io/v4`
- **Official documentation:** [Import File](https://next.developer.frame.io/platform/api-reference/files/import-file)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `account_id` | path | `string` | yes |
| `folder_id` | path | `string` | yes |
| `data` | body | `object` | yes |

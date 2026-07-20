# Copy File with Frame.io v4

Copies a file in Frame.io v4.

## Endpoint

- **Method:** `POST`
- **Path:** `/accounts/:accountId/files/:fileId/copy`
- **Base URL:** `https://api.frame.io/v4`
- **Official documentation:** [Copy File](https://next.developer.frame.io/platform/api-reference/files/copy)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `account_id` | path | `string` | yes |
| `file_id` | path | `string` | yes |
| `copy_metadata` | query | `boolean` | no |
| `copy_comments` | query | `string` | no |
| `data` | body | `object` | no |

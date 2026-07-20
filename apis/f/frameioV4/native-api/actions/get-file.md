# Get File with Frame.io v4

Retrieves a file from Frame.io v4.

## Endpoint

- **Method:** `GET`
- **Path:** `/accounts/:accountId/files/:fileId`
- **Base URL:** `https://api.frame.io/v4`
- **Official documentation:** [Get File](https://next.developer.frame.io/platform/api-reference/files/show)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `account_id` | path | `string` | yes |
| `file_id` | path | `string` | yes |
| `include` | query | `string` | no |

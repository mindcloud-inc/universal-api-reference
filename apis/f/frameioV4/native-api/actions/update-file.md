# Update File with Frame.io v4

Updates an existing file in Frame.io v4.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/accounts/:accountId/files/:fileId`
- **Base URL:** `https://api.frame.io/v4`
- **Official documentation:** [Update File](https://next.developer.frame.io/platform/api-reference/files/update)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `account_id` | path | `string` | yes |
| `file_id` | path | `string` | yes |
| `data` | body | `object` | yes |

# Move File with Frame.io v4

Moves a file in Frame.io v4.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/accounts/:accountId/files/:fileId/move`
- **Base URL:** `https://api.frame.io/v4`
- **Official documentation:** [Move File](https://next.developer.frame.io/platform/api-reference/files/move)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `account_id` | path | `string` | yes |
| `file_id` | path | `string` | yes |
| `data` | body | `object` | yes |

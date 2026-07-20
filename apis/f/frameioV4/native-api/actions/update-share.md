# Update Share with Frame.io v4

Updates an existing share in Frame.io v4.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/accounts/:accountId/shares/:shareId`
- **Base URL:** `https://api.frame.io/v4`
- **Official documentation:** [Update Share](https://next.developer.frame.io/platform/api-reference/shares/update)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `account_id` | path | `string` | yes |
| `share_id` | path | `string` | yes |
| `data` | body | `object` | yes |

# Create Workspace with Frame.io v4

Creates a new workspace in Frame.io v4.

## Endpoint

- **Method:** `POST`
- **Path:** `/accounts/:accountId/workspaces`
- **Base URL:** `https://api.frame.io/v4`
- **Official documentation:** [Create Workspace](https://next.developer.frame.io/platform/api-reference/workspaces/create)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `account_id` | path | `string` | yes |
| `data` | body | `object` | yes |

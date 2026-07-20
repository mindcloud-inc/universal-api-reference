# Create Share with Frame.io v4

Creates a new share in Frame.io v4.

## Endpoint

- **Method:** `POST`
- **Path:** `/accounts/:accountId/projects/:projectId/shares`
- **Base URL:** `https://api.frame.io/v4`
- **Official documentation:** [Create Share](https://next.developer.frame.io/platform/api-reference/shares/create)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `account_id` | path | `string` | yes |
| `project_id` | path | `string` | yes |
| `data` | body | `object` | yes |

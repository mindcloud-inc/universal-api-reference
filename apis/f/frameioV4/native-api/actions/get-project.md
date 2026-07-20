# Get Project with Frame.io v4

Retrieves a project from Frame.io v4.

## Endpoint

- **Method:** `GET`
- **Path:** `/accounts/:accountId/projects/:projectId`
- **Base URL:** `https://api.frame.io/v4`
- **Official documentation:** [Get Project](https://next.developer.frame.io/platform/api-reference/projects/show)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `account_id` | path | `string` | yes |
| `project_id` | path | `string` | yes |
| `include` | query | `string` | no |

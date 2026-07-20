# Update Project with Frame.io v4

Updates an existing project in Frame.io v4.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/accounts/:accountId/projects/:projectId`
- **Base URL:** `https://api.frame.io/v4`
- **Official documentation:** [Update Project](https://next.developer.frame.io/platform/api-reference/projects/update)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `account_id` | path | `string` | yes |
| `project_id` | path | `string` | yes |
| `data` | body | `object` | yes |

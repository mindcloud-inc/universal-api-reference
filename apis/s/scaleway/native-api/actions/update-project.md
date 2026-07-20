# Update Project with Scaleway

Updates an existing project in Scaleway.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/account/v3/projects/:project_id`
- **Base URL:** `https://api.scaleway.com`
- **Official documentation:** [Update Project](https://www.scaleway.com/en/developers/api/account/project-api/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `project_id` | path | `string` | yes |
| `name` | body | `string` | no |

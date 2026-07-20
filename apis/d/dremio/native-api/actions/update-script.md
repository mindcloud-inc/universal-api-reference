# Update Script with Dremio

Updates an existing script in a Dremio project.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/projects/:project_id/scripts/:id`
- **Base URL:** `https://api.dremio.cloud/v0`
- **Official documentation:** [Update Script](https://docs.dremio.com/dremio-cloud/api/scripts/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `project_id` | path | `string` | yes |

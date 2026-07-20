# Update Engine with Dremio

Updates an existing engine in a Dremio project.

## Endpoint

- **Method:** `PUT`
- **Path:** `/projects/:project_id/engines/:id`
- **Base URL:** `https://api.dremio.cloud/v0`
- **Official documentation:** [Update Engine](https://docs.dremio.com/dremio-cloud/api/engines/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `engine` | body | `object` | yes |
| `id` | path | `string` | yes |
| `project_id` | path | `string` | yes |

# Update Reflection with Dremio

Updates an existing reflection in a Dremio project.

## Endpoint

- **Method:** `PUT`
- **Path:** `/projects/:project_id/reflection/:id`
- **Base URL:** `https://api.dremio.cloud/v0`
- **Official documentation:** [Update Reflection](https://docs.dremio.com/dremio-cloud/api/reflection/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `project_id` | path | `string` | yes |
| `reflection` | body | `object` | yes |

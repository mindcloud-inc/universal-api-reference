# Delete Reflection with Dremio

Deletes an existing reflection from a Dremio project.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/projects/:project_id/reflection/:id`
- **Base URL:** `https://api.dremio.cloud/v0`
- **Official documentation:** [Delete Reflection](https://docs.dremio.com/dremio-cloud/api/reflection/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `project_id` | path | `string` | yes |

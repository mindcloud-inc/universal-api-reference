# Delete Engine with Dremio

Deletes an existing engine from a Dremio project.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/projects/:project_id/engines/:id`
- **Base URL:** `https://api.dremio.cloud/v0`
- **Official documentation:** [Delete Engine](https://docs.dremio.com/dremio-cloud/api/engines/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `project_id` | path | `string` | yes |

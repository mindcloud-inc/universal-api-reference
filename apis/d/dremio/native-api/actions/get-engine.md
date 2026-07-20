# Get Engine with Dremio

Retrieves an engine from a Dremio project.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:project_id/engines/:id`
- **Base URL:** `https://api.dremio.cloud/v0`
- **Official documentation:** [Get Engine](https://docs.dremio.com/dremio-cloud/api/engines/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `project_id` | path | `string` | yes |

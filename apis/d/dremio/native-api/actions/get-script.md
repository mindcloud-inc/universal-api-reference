# Get Script with Dremio

Retrieves a script from a Dremio project.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:project_id/scripts/:id`
- **Base URL:** `https://api.dremio.cloud/v0`
- **Official documentation:** [Get Script](https://docs.dremio.com/dremio-cloud/api/scripts/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `project_id` | path | `string` | yes |

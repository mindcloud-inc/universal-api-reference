# Get Script Grants with Dremio

Retrieves grants for a script in Dremio.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:project_id/scripts/:id/grants`
- **Base URL:** `https://api.dremio.cloud/v0`
- **Official documentation:** [Get Script Grants](https://docs.dremio.com/dremio-cloud/api/scripts/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `project_id` | path | `string` | yes |

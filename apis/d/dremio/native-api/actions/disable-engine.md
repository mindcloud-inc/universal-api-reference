# Disable Engine with Dremio

Disables an engine in a Dremio project.

## Endpoint

- **Method:** `PUT`
- **Path:** `/projects/:project_id/engines/:id/disable`
- **Base URL:** `https://api.dremio.cloud/v0`
- **Official documentation:** [Disable Engine](https://docs.dremio.com/dremio-cloud/api/engines/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `project_id` | path | `string` | yes |

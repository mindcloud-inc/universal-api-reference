# Refresh Reflection with Dremio

Refreshes an existing reflection in a Dremio project.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/:project_id/reflection/:id/refresh`
- **Base URL:** `https://api.dremio.cloud/v0`
- **Official documentation:** [Refresh Reflection](https://docs.dremio.com/dremio-cloud/api/reflection/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `project_id` | path | `string` | yes |

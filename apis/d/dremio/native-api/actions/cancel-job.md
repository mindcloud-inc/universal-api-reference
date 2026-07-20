# Cancel Job with Dremio

Cancels a job in a Dremio project.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/:project_id/job/:id/cancel`
- **Base URL:** `https://api.dremio.cloud/v0`
- **Official documentation:** [Cancel Job](https://docs.dremio.com/dremio-cloud/api/job/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `project_id` | path | `string` | yes |

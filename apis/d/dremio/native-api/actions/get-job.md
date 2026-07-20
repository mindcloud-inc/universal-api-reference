# Get Job with Dremio

Retrieves a job from a Dremio project.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:project_id/job/:id`
- **Base URL:** `https://api.dremio.cloud/v0`
- **Official documentation:** [Get Job](https://docs.dremio.com/dremio-cloud/api/job/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `project_id` | path | `string` | yes |

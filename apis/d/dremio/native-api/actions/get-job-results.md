# Get Job Results with Dremio

Retrieves results for a Dremio job.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:project_id/job/:id/results`
- **Base URL:** `https://api.dremio.cloud/v0`
- **Official documentation:** [Get Job Results](https://docs.dremio.com/dremio-cloud/api/job/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `project_id` | path | `string` | yes |

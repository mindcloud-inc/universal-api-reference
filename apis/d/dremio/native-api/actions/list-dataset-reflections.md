# List Dataset Reflections with Dremio

Retrieves reflections for a dataset in Dremio.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:project_id/dataset/:datasetId/reflection`
- **Base URL:** `https://api.dremio.cloud/v0`
- **Official documentation:** [List Dataset Reflections](https://docs.dremio.com/dremio-cloud/api/reflection/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `datasetId` | path | `string` | yes |
| `project_id` | path | `string` | yes |

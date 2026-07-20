# Delete Sample with Frameshift

Deletes an existing sample from Frameshift.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v1/projects/:project_id/samples/:sample_id`
- **Base URL:** `https://mosaic.frameshift.io/api`
- **Official documentation:** [Delete Sample](https://mosaic.frameshift.io/api/#api-Samples-DeleteSample)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `project_id` | path | `number` | yes |
| `sample_id` | path | `number` | yes |

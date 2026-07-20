# Get Sample QC Stats with Frameshift

Retrieves sample QC statistics from Frameshift.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/projects/:project_id/sample-qc-stats`
- **Base URL:** `https://mosaic.frameshift.io/api`
- **Official documentation:** [Get Sample QC Stats](https://mosaic.frameshift.io/api/#api-Samples-sampleQcStats)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `project_id` | path | `number` | yes |
| `filter` | query | `string` | yes |

# Get Sample with Frameshift

Retrieves detailed sample information from Frameshift.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/projects/:project_id/samples/:sample_id`
- **Base URL:** `https://mosaic.frameshift.io/api`
- **Official documentation:** [Get Sample](https://mosaic.frameshift.io/api/#api-Samples-GetSample)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `project_id` | path | `number` | yes |
| `sample_id` | path | `number` | yes |
| `attach_summary_data` | query | `boolean` | no |

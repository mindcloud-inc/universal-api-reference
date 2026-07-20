# Update Sample with Frameshift

Updates an existing sample in Frameshift.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/projects/:project_id/samples/:sample_id`
- **Base URL:** `https://mosaic.frameshift.io/api`
- **Official documentation:** [Update Sample](https://mosaic.frameshift.io/api/#api-Samples-PutSample)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `project_id` | path | `number` | yes |
| `sample_id` | path | `number` | yes |
| `name` | body | `string` | no |
| `description` | body | `string` | no |

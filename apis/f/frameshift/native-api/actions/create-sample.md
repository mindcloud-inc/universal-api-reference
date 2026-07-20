# Create Sample with Frameshift

Creates a new sample in Frameshift.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/projects/:project_id/samples`
- **Base URL:** `https://mosaic.frameshift.io/api`
- **Official documentation:** [Create Sample](https://mosaic.frameshift.io/api/#api-Samples-CreateSample)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `project_id` | path | `number` | yes |
| `name` | body | `string` | yes |
| `description` | body | `string` | no |

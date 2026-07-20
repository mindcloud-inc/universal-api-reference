# Create Reflection with Dremio

Creates a new reflection in a Dremio project.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/:project_id/reflection`
- **Base URL:** `https://api.dremio.cloud/v0`
- **Official documentation:** [Create Reflection](https://docs.dremio.com/dremio-cloud/api/reflection/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `datasetId` | body | `string` | yes |
| `name` | body | `string` | yes |
| `project_id` | path | `string` | yes |
| `type` | body | `string` | yes |

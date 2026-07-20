# Create Engine with Dremio

Creates a new engine in a Dremio project.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/:project_id/engines`
- **Base URL:** `https://api.dremio.cloud/v0`
- **Official documentation:** [Create Engine](https://docs.dremio.com/dremio-cloud/api/engines/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `engine` | body | `object` | yes |
| `project_id` | path | `string` | yes |

# Get Source with Dremio

Retrieves a source from a Dremio project.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:project_id/catalog/:id`
- **Base URL:** `https://api.dremio.cloud/v0`
- **Official documentation:** [Get Source](https://docs.dremio.com/dremio-cloud/api/catalog/source/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `project_id` | path | `string` | yes |

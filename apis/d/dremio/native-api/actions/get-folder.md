# Get Folder with Dremio

Retrieves a folder from a Dremio project.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:project_id/catalog/:id`
- **Base URL:** `https://api.dremio.cloud/v0`
- **Official documentation:** [Get Folder](https://docs.dremio.com/dremio-cloud/api/catalog/folder/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `project_id` | path | `string` | yes |

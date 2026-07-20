# Get Catalog Grants with Dremio

Retrieves grants for a catalog entry in Dremio.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:project_id/catalog/:id/grants`
- **Base URL:** `https://api.dremio.cloud/v0`
- **Official documentation:** [Get Catalog Grants](https://docs.dremio.com/dremio-cloud/api/catalog/grants/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `project_id` | path | `string` | yes |

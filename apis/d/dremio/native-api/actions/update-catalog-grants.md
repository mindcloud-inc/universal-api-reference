# Update Catalog Grants with Dremio

Updates grants for a catalog entry in Dremio.

## Endpoint

- **Method:** `PUT`
- **Path:** `/projects/:project_id/catalog/:id/grants`
- **Base URL:** `https://api.dremio.cloud/v0`
- **Official documentation:** [Update Catalog Grants](https://docs.dremio.com/dremio-cloud/api/catalog/grants/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `grants` | body | `list<object>` | yes |
| `id` | path | `string` | yes |
| `project_id` | path | `string` | yes |

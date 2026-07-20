# Search with Dremio

Searches a Dremio project for matching resources.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/:project_id/search`
- **Base URL:** `https://api.dremio.cloud/v0`
- **Official documentation:** [Search](https://docs.dremio.com/dremio-cloud/api/search/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `maxResults` | body | `number` | no |
| `project_id` | path | `string` | yes |
| `query` | body | `string` | yes |

# Update Project with Dremio

Updates an existing project in Dremio.

## Endpoint

- **Method:** `PUT`
- **Path:** `/projects/:id`
- **Base URL:** `https://api.dremio.cloud/v0`
- **Official documentation:** [Update Project](https://docs.dremio.com/dremio-cloud/api/projects/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `project` | body | `object` | yes |

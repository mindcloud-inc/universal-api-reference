# Get Reflection Summary with Dremio

Retrieves a reflection summary from Dremio.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:project_id/reflection/:id`
- **Base URL:** `https://api.dremio.cloud/v0`
- **Official documentation:** [Get Reflection Summary](https://docs.dremio.com/dremio-cloud/api/reflection/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `project_id` | path | `string` | yes |

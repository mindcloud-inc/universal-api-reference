# Update Script Grants with Dremio

Updates grants for a script in Dremio.

## Endpoint

- **Method:** `PUT`
- **Path:** `/projects/:project_id/scripts/:id/grants`
- **Base URL:** `https://api.dremio.cloud/v0`
- **Official documentation:** [Update Script Grants](https://docs.dremio.com/dremio-cloud/api/scripts/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `grants` | body | `list<object>` | yes |
| `id` | path | `string` | yes |
| `project_id` | path | `string` | yes |

# Clear Source Permission Cache with Dremio

Clears a source permission cache in Dremio.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/projects/:project_id/source/:source_name/permission-cache`
- **Base URL:** `https://api.dremio.cloud/v0`
- **Official documentation:** [Clear Source Permission Cache](https://docs.dremio.com/dremio-cloud/api/source/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `project_id` | path | `string` | yes |
| `source_name` | path | `string` | yes |

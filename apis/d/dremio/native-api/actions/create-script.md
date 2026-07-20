# Create Script with Dremio

Creates a new script in a Dremio project.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/:project_id/scripts`
- **Base URL:** `https://api.dremio.cloud/v0`
- **Official documentation:** [Create Script](https://docs.dremio.com/dremio-cloud/api/scripts/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `content` | body | `string` | yes |
| `name` | body | `string` | yes |
| `project_id` | path | `string` | yes |

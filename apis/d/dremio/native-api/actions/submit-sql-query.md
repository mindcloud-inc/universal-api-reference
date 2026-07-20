# Submit SQL Query with Dremio

Creates a SQL job in a Dremio project.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/:project_id/sql`
- **Base URL:** `https://api.dremio.cloud/v0`
- **Official documentation:** [Submit SQL Query](https://docs.dremio.com/dremio-cloud/api/sql/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `project_id` | path | `string` | yes |
| `sql` | body | `string` | yes |

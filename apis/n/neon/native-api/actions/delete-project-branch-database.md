# Delete database with Neon

Deletes a database from Neon.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/projects/:project_id/branches/:branch_id/databases/:database_name`
- **Base URL:** `https://console.neon.tech/api/v2`
- **Official documentation:** [Delete database](https://api-docs.neon.tech/reference/deleteprojectbranchdatabase)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Neon API parameter project_id |
| `branch_id` | path | `string` | yes | Neon API parameter branch_id |
| `database_name` | path | `string` | yes | Neon API parameter database_name |

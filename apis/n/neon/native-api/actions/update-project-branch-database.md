# Update database with Neon

Updates a database in Neon.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/projects/:project_id/branches/:branch_id/databases/:database_name`
- **Base URL:** `https://console.neon.tech/api/v2`
- **Official documentation:** [Update database](https://api-docs.neon.tech/reference/updateprojectbranchdatabase)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Neon API parameter project_id |
| `branch_id` | path | `string` | yes | Neon API parameter branch_id |
| `database_name` | path | `string` | yes | Neon API parameter database_name |
| `database` | body | `object` | yes | Neon API parameter database |

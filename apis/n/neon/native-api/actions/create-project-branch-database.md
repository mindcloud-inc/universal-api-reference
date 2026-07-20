# Create database with Neon

Creates a database in Neon.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/:project_id/branches/:branch_id/databases`
- **Base URL:** `https://console.neon.tech/api/v2`
- **Official documentation:** [Create database](https://api-docs.neon.tech/reference/createprojectbranchdatabase)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Neon API parameter project_id |
| `branch_id` | path | `string` | yes | Neon API parameter branch_id |
| `database` | body | `object` | yes | Neon API parameter database |

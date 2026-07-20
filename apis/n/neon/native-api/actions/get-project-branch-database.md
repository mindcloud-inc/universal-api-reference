# Retrieve database details with Neon

Retrieves database details from Neon.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:project_id/branches/:branch_id/databases/:database_name`
- **Base URL:** `https://console.neon.tech/api/v2`
- **Official documentation:** [Retrieve database details](https://api-docs.neon.tech/reference/getprojectbranchdatabase)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Neon API parameter project_id |
| `branch_id` | path | `string` | yes | Neon API parameter branch_id |
| `database_name` | path | `string` | yes | Neon API parameter database_name |

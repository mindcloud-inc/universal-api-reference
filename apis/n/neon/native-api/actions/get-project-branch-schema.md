# Retrieve database schema with Neon

Retrieves database schema from Neon.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:project_id/branches/:branch_id/schema`
- **Base URL:** `https://console.neon.tech/api/v2`
- **Official documentation:** [Retrieve database schema](https://api-docs.neon.tech/reference/getprojectbranchschema)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Neon API parameter project_id |
| `branch_id` | path | `string` | yes | Neon API parameter branch_id |
| `db_name` | query | `string` | yes | Neon API parameter db_name |
| `lsn` | query | `string` | no | Neon API parameter lsn |
| `timestamp` | query | `date` | no | Neon API parameter timestamp |
| `format` | query | `string` | no | Neon API parameter format |

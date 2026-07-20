# Compare database schema with Neon

Compares database schemas in Neon.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:project_id/branches/:branch_id/compare_schema`
- **Base URL:** `https://console.neon.tech/api/v2`
- **Official documentation:** [Compare database schema](https://api-docs.neon.tech/reference/getprojectbranchschemacomparison)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Neon API parameter project_id |
| `branch_id` | path | `string` | yes | Neon API parameter branch_id |
| `base_branch_id` | query | `string` | no | Neon API parameter base_branch_id |
| `db_name` | query | `string` | yes | Neon API parameter db_name |
| `lsn` | query | `string` | no | Neon API parameter lsn |
| `timestamp` | query | `date` | no | Neon API parameter timestamp |
| `base_lsn` | query | `string` | no | Neon API parameter base_lsn |
| `base_timestamp` | query | `date` | no | Neon API parameter base_timestamp |

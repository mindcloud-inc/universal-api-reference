# Update Neon Data API with Neon

Updates Neon Data API configuration in Neon.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/projects/:project_id/branches/:branch_id/data-api/:database_name`
- **Base URL:** `https://console.neon.tech/api/v2`
- **Official documentation:** [Update Neon Data API](https://api-docs.neon.tech/reference/updateprojectbranchdataapi)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Neon API parameter project_id |
| `branch_id` | path | `string` | yes | Neon API parameter branch_id |
| `database_name` | path | `string` | yes | Neon API parameter database_name |
| `settings` | body | `object` | no | Neon API parameter settings |

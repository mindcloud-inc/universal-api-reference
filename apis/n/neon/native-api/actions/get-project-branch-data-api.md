# Get Neon Data API with Neon

Retrieves Neon Data API configuration from Neon.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:project_id/branches/:branch_id/data-api/:database_name`
- **Base URL:** `https://console.neon.tech/api/v2`
- **Official documentation:** [Get Neon Data API](https://api-docs.neon.tech/reference/getprojectbranchdataapi)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Neon API parameter project_id |
| `branch_id` | path | `string` | yes | Neon API parameter branch_id |
| `database_name` | path | `string` | yes | Neon API parameter database_name |

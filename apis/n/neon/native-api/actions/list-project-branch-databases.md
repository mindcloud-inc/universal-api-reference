# List databases with Neon

Retrieves databases from Neon.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:project_id/branches/:branch_id/databases`
- **Base URL:** `https://console.neon.tech/api/v2`
- **Official documentation:** [List databases](https://api-docs.neon.tech/reference/listprojectbranchdatabases)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Neon API parameter project_id |
| `branch_id` | path | `string` | yes | Neon API parameter branch_id |

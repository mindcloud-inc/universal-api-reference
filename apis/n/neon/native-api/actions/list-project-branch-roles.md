# List roles with Neon

Retrieves roles from Neon.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:project_id/branches/:branch_id/roles`
- **Base URL:** `https://console.neon.tech/api/v2`
- **Official documentation:** [List roles](https://api-docs.neon.tech/reference/listprojectbranchroles)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Neon API parameter project_id |
| `branch_id` | path | `string` | yes | Neon API parameter branch_id |

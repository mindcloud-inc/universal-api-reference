# List branch endpoints with Neon

Retrieves branch endpoints from Neon.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:project_id/branches/:branch_id/endpoints`
- **Base URL:** `https://console.neon.tech/api/v2`
- **Official documentation:** [List branch endpoints](https://api-docs.neon.tech/reference/listprojectbranchendpoints)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Neon API parameter project_id |
| `branch_id` | path | `string` | yes | Neon API parameter branch_id |

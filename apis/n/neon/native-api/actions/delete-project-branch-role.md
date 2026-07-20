# Delete role with Neon

Deletes a role from Neon.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/projects/:project_id/branches/:branch_id/roles/:role_name`
- **Base URL:** `https://console.neon.tech/api/v2`
- **Official documentation:** [Delete role](https://api-docs.neon.tech/reference/deleteprojectbranchrole)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Neon API parameter project_id |
| `branch_id` | path | `string` | yes | Neon API parameter branch_id |
| `role_name` | path | `string` | yes | Neon API parameter role_name |

# Retrieve role details with Neon

Retrieves role details from Neon.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:project_id/branches/:branch_id/roles/:role_name`
- **Base URL:** `https://console.neon.tech/api/v2`
- **Official documentation:** [Retrieve role details](https://api-docs.neon.tech/reference/getprojectbranchrole)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Neon API parameter project_id |
| `branch_id` | path | `string` | yes | Neon API parameter branch_id |
| `role_name` | path | `string` | yes | Neon API parameter role_name |

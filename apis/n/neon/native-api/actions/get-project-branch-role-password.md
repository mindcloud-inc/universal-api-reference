# Retrieve role password with Neon

Retrieves a role password from Neon.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:project_id/branches/:branch_id/roles/:role_name/reveal_password`
- **Base URL:** `https://console.neon.tech/api/v2`
- **Official documentation:** [Retrieve role password](https://api-docs.neon.tech/reference/getprojectbranchrolepassword)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Neon API parameter project_id |
| `branch_id` | path | `string` | yes | Neon API parameter branch_id |
| `role_name` | path | `string` | yes | Neon API parameter role_name |

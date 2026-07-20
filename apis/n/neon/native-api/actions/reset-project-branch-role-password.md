# Reset role password with Neon

Resets a role password in Neon.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/:project_id/branches/:branch_id/roles/:role_name/reset_password`
- **Base URL:** `https://console.neon.tech/api/v2`
- **Official documentation:** [Reset role password](https://api-docs.neon.tech/reference/resetprojectbranchrolepassword)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Neon API parameter project_id |
| `branch_id` | path | `string` | yes | Neon API parameter branch_id |
| `role_name` | path | `string` | yes | Neon API parameter role_name |

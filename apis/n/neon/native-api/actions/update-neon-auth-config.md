# Update auth configuration with Neon

Updates auth configuration in Neon.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/projects/:project_id/branches/:branch_id/auth/config`
- **Base URL:** `https://console.neon.tech/api/v2`
- **Official documentation:** [Update auth configuration](https://api-docs.neon.tech/reference/updateneonauthconfig)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Neon API parameter project_id |
| `branch_id` | path | `string` | yes | Neon API parameter branch_id |
| `name` | body | `string` | yes | Neon API parameter name |

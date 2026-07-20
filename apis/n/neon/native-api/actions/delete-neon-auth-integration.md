# Delete integration with auth provider with Neon

Deletes an auth provider integration from Neon.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/projects/:project_id/auth/integration/:auth_provider`
- **Base URL:** `https://console.neon.tech/api/v2`
- **Official documentation:** [Delete integration with auth provider](https://api-docs.neon.tech/reference/deleteneonauthintegration)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Neon API parameter project_id |
| `auth_provider` | path | `list` | yes | Neon API parameter auth_provider Accepted values: `0`, `1`, `2`, `3`. |
| `delete_data` | body | `boolean` | no | Neon API parameter delete_data |

# Enable Neon Auth for the branch with Neon

Enables Neon Auth for a branch in Neon.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/:project_id/branches/:branch_id/auth`
- **Base URL:** `https://console.neon.tech/api/v2`
- **Official documentation:** [Enable Neon Auth for the branch](https://api-docs.neon.tech/reference/createneonauth)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Neon API parameter project_id |
| `branch_id` | path | `string` | yes | Neon API parameter branch_id |
| `auth_provider` | body | `list` | yes | Neon API parameter auth_provider Accepted values: `0`, `1`, `2`, `3`. |
| `database_name` | body | `string` | no | Neon API parameter database_name |

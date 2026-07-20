# Delete auth user with Neon

Deletes an auth user from Neon.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/projects/:project_id/branches/:branch_id/auth/users/:auth_user_id`
- **Base URL:** `https://console.neon.tech/api/v2`
- **Official documentation:** [Delete auth user](https://api-docs.neon.tech/reference/deletebranchneonauthuser)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Neon API parameter project_id |
| `branch_id` | path | `string` | yes | Neon API parameter branch_id |
| `auth_user_id` | path | `string` | yes | Neon API parameter auth_user_id |

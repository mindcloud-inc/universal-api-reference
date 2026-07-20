# Update auth user role with Neon

Updates an auth user role in Neon.

## Endpoint

- **Method:** `PUT`
- **Path:** `/projects/:project_id/branches/:branch_id/auth/users/:auth_user_id/role`
- **Base URL:** `https://console.neon.tech/api/v2`
- **Official documentation:** [Update auth user role](https://api-docs.neon.tech/reference/updateneonauthuserrole)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Neon API parameter project_id |
| `branch_id` | path | `string` | yes | Neon API parameter branch_id |
| `auth_user_id` | path | `string` | yes | Neon API parameter auth_user_id |
| `roles[]` | body | `array<string>` | yes | Neon API parameter roles |

# Create new auth user with Neon

Creates an auth user in Neon.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/:project_id/branches/:branch_id/auth/users`
- **Base URL:** `https://console.neon.tech/api/v2`
- **Official documentation:** [Create new auth user](https://api-docs.neon.tech/reference/createbranchneonauthnewuser)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Neon API parameter project_id |
| `branch_id` | path | `string` | yes | Neon API parameter branch_id |
| `email` | body | `string` | yes | Neon API parameter email |
| `name` | body | `string` | no | Neon API parameter name |

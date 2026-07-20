# Create new auth user with Neon

Creates an auth user in Neon.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/auth/user`
- **Base URL:** `https://console.neon.tech/api/v2`
- **Official documentation:** [Create new auth user](https://api-docs.neon.tech/reference/createneonauthnewuser)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | body | `string` | yes | Neon API parameter project_id |
| `auth_provider` | body | `list` | yes | Neon API parameter auth_provider Accepted values: `0`, `1`, `2`, `3`. |
| `email` | body | `string` | yes | Neon API parameter email |
| `name` | body | `string` | no | Neon API parameter name |

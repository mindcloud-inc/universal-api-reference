# Create Neon Auth integration with Neon

Creates Neon Auth integration in Neon.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/auth/create`
- **Base URL:** `https://console.neon.tech/api/v2`
- **Official documentation:** [Create Neon Auth integration](https://api-docs.neon.tech/reference/createneonauthintegration)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `auth_provider` | body | `list` | yes | Neon API parameter auth_provider Accepted values: `0`, `1`, `2`, `3`. |
| `project_id` | body | `string` | yes | Neon API parameter project_id |
| `branch_id` | body | `string` | yes | Neon API parameter branch_id |
| `database_name` | body | `string` | no | Neon API parameter database_name |
| `role_name` | body | `string` | no | Neon API parameter role_name |

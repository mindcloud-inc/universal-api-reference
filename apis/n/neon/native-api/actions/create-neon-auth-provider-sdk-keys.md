# Create Auth Provider SDK keys with Neon

Creates auth provider SDK keys in Neon.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/auth/keys`
- **Base URL:** `https://console.neon.tech/api/v2`
- **Official documentation:** [Create Auth Provider SDK keys](https://api-docs.neon.tech/reference/createneonauthprovidersdkkeys)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | body | `string` | yes | Neon API parameter project_id |
| `auth_provider` | body | `list` | yes | Neon API parameter auth_provider Accepted values: `0`, `1`, `2`, `3`. |

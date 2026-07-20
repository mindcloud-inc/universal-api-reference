# Create User with Permit.io

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/facts/:projId/:envId/users`
- **Base URL:** `https://api.permit.io`
- **Official documentation:** [Create User](https://api.permit.io/scalar)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projId` | path | `string` | yes | Permit project identifier or key. |
| `envId` | path | `string` | yes | Permit environment identifier or key. |
| `key` | body | `string` | yes | Unique user key within the Permit environment. |
| `email` | body | `string` | no | User email address. |
| `first_name` | body | `string` | no | User first name. |
| `last_name` | body | `string` | no | User last name. |
| `attributes` | body | `object` | no | Custom user attributes object. |
| `role_assignments[]` | body | `array<object>` | no | Initial role assignments array. |

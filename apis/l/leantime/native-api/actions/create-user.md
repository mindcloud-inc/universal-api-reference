# Create User with Leantime

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `{workspaceUrl}/api/jsonrpc`
- **Official documentation:** [Create User](https://docs.leantime.io/api/classes/Leantime/Domain/Users/Services/Users)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `params.values.user` | body | `string` | yes | Username or email for the new user. |
| `params.values.password` | body | `string` | yes | Password for the new user. |
| `params.values.role` | body | `number` | yes | Numeric role key for the user. |
| `params.values.firstname` | body | `string` | no | User first name. |
| `params.values.lastname` | body | `string` | no | User last name. |
| `params.values.phone` | body | `string` | no | User phone number. |
| `params.values.status` | body | `string` | no | User status code. |

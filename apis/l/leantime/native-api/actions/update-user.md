# Update User with Leantime

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `{workspaceUrl}/api/jsonrpc`
- **Official documentation:** [Update User](https://docs.leantime.io/api/classes/Leantime/Domain/Users/Services/Users)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | body | `number` | yes | The Leantime user id to update. |
| `params.values.user` | body | `string` | yes | Username or email for the user. |
| `params.values.role` | body | `number` | yes | Numeric role key for the user. |
| `params.values.status` | body | `string` | yes | User status code. |
| `params.values.clientId` | body | `number` | yes | Client id assigned to the user. |
| `params.values.firstname` | body | `string` | yes | User first name. |
| `params.values.lastname` | body | `string` | yes | User last name. |
| `params.values.phone` | body | `string` | no | User phone number. |
| `params.values.password` | body | `string` | no | Optional replacement password. |

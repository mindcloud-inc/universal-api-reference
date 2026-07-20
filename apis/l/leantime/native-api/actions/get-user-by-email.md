# Get User by Email with Leantime

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `{workspaceUrl}/api/jsonrpc`
- **Official documentation:** [Get User by Email](https://docs.leantime.io/api/classes/Leantime/Domain/Users/Services/Users)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `params.email` | body | `string` | yes | The email address to look up. |
| `params.status` | body | `string` | no | User status code filter. |

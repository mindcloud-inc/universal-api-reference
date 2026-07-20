# List Database Users with ServerAvatar

Retrieves database users from ServerAvatar.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizations/{{organization}}/servers/{{server}}/databases/{{database}}/database-users`
- **Base URL:** `https://api.serveravatar.com`
- **Official documentation:** [List Database Users](https://serveravatar.com/api-docs/endpoint/database-user/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `organization` | path | `string` | yes |
| `server` | path | `string` | yes |
| `database` | path | `string` | yes |

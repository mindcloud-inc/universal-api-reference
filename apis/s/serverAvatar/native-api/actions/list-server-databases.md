# List Server Databases with ServerAvatar

Retrieves server databases from ServerAvatar.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizations/{{organization}}/servers/{{server}}/databases`
- **Base URL:** `https://api.serveravatar.com`
- **Official documentation:** [List Server Databases](https://serveravatar.com/api-docs/endpoint/database/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `organization` | path | `string` | yes |
| `server` | path | `string` | yes |

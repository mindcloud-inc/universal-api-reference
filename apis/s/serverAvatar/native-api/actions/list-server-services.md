# List Server Services with ServerAvatar

Retrieves server services from ServerAvatar.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizations/{{organization}}/servers/{{server}}/services`
- **Base URL:** `https://api.serveravatar.com`
- **Official documentation:** [List Server Services](https://serveravatar.com/api-docs/endpoint/server/services.html)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `organization` | path | `string` | yes |
| `server` | path | `string` | yes |

# List Server Applications with ServerAvatar

Retrieves server applications from ServerAvatar.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizations/{{organization}}/servers/{{server}}/applications`
- **Base URL:** `https://api.serveravatar.com`
- **Official documentation:** [List Server Applications](https://serveravatar.com/api-docs/endpoint/application/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `organization` | path | `string` | yes |
| `server` | path | `string` | yes |

# List Application Users with ServerAvatar

Retrieves application users from ServerAvatar.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizations/{{organization}}/servers/{{server}}/system-users`
- **Base URL:** `https://api.serveravatar.com`
- **Official documentation:** [List Application Users](https://serveravatar.com/api-docs/endpoint/application-user/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `organization` | path | `string` | yes |
| `server` | path | `string` | yes |

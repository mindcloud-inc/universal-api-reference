# List Server Alerts with ServerAvatar

Retrieves server alerts from ServerAvatar.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizations/{{organization}}/servers/{{server}}/alert`
- **Base URL:** `https://api.serveravatar.com`
- **Official documentation:** [List Server Alerts](https://serveravatar.com/api-docs/endpoint/server/alerts.html)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `organization` | path | `string` | yes |
| `server` | path | `string` | yes |

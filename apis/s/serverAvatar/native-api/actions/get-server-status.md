# Get Server Status with ServerAvatar

Retrieves server status from ServerAvatar.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizations/{{organization}}/servers/{{server}}/status`
- **Base URL:** `https://api.serveravatar.com`
- **Official documentation:** [Get Server Status](https://serveravatar.com/api-docs/endpoint/server/status.html)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `organization` | path | `string` | yes |
| `server` | path | `string` | yes |

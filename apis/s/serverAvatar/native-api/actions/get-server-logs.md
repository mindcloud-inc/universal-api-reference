# Get Server Logs with ServerAvatar

Retrieves server logs from ServerAvatar.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizations/{{organization}}/servers/{{server}}/logs`
- **Base URL:** `https://api.serveravatar.com`
- **Official documentation:** [Get Server Logs](https://serveravatar.com/api-docs/endpoint/server/logs.html)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `organization` | path | `string` | yes |
| `server` | path | `string` | yes |

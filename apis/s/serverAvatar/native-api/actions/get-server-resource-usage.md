# Get Server Resource Usage with ServerAvatar

Retrieves server resource usage from ServerAvatar.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizations/{{organization}}/servers/{{server}}/usage`
- **Base URL:** `https://api.serveravatar.com`
- **Official documentation:** [Get Server Resource Usage](https://serveravatar.com/api-docs/endpoint/server/resources-usage.html)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `organization` | path | `string` | yes |
| `server` | path | `string` | yes |

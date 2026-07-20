# Get Application Log Sizes with ServerAvatar

Retrieves application log sizes from ServerAvatar.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizations/{{organization}}/servers/{{server}}/applications/{{application}}/log-sizes`
- **Base URL:** `https://api.serveravatar.com`
- **Official documentation:** [Get Application Log Sizes](https://serveravatar.com/api-docs/endpoint/application/logs.html)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `organization` | path | `string` | yes |
| `server` | path | `string` | yes |
| `application` | path | `string` | yes |

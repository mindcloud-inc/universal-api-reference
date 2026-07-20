# Get Application with ServerAvatar

Retrieves an application from ServerAvatar.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizations/{{organization}}/servers/{{server}}/applications/{{application}}`
- **Base URL:** `https://api.serveravatar.com`
- **Official documentation:** [Get Application](https://serveravatar.com/api-docs/endpoint/application/show.html)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `organization` | path | `string` | yes |
| `server` | path | `string` | yes |
| `application` | path | `string` | yes |

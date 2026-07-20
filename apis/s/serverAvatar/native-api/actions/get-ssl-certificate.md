# Get SSL Certificate with ServerAvatar

Retrieves an SSL certificate from ServerAvatar.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizations/{{organization}}/servers/{{server}}/applications/{{application}}/ssl`
- **Base URL:** `https://api.serveravatar.com`
- **Official documentation:** [Get SSL Certificate](https://serveravatar.com/api-docs/endpoint/ssl/show.html)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `organization` | path | `string` | yes |
| `server` | path | `string` | yes |
| `application` | path | `string` | yes |

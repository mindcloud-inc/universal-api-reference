# List Application Domains with ServerAvatar

Retrieves application domains from ServerAvatar.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizations/{{organization}}/servers/{{server}}/applications/{{application}}/application-domains`
- **Base URL:** `https://api.serveravatar.com`
- **Official documentation:** [List Application Domains](https://serveravatar.com/api-docs/endpoint/application-domain/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `organization` | path | `string` | yes |
| `server` | path | `string` | yes |
| `application` | path | `string` | yes |

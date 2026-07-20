# Get Firewall Status with ServerAvatar

Retrieves firewall details from ServerAvatar.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizations/{{organization}}/servers/{{server}}/firewall`
- **Base URL:** `https://api.serveravatar.com`
- **Official documentation:** [Get Firewall Status](https://serveravatar.com/api-docs/endpoint/firewall/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `organization` | path | `string` | yes |
| `server` | path | `string` | yes |

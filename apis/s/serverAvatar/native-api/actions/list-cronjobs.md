# List Cronjobs with ServerAvatar

Retrieves cronjobs from ServerAvatar.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizations/{{organization}}/servers/{{server}}/cronjobs`
- **Base URL:** `https://api.serveravatar.com`
- **Official documentation:** [List Cronjobs](https://serveravatar.com/api-docs/endpoint/cronjob/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `organization` | path | `string` | yes |
| `server` | path | `string` | yes |

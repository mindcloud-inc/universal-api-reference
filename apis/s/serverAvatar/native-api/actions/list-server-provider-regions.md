# List Server Provider Regions with ServerAvatar

Retrieves server provider regions from ServerAvatar.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizations/{{organization}}/cloud-server-providers/{{cloudServerProvider}}/regions`
- **Base URL:** `https://api.serveravatar.com`
- **Official documentation:** [List Server Provider Regions](https://serveravatar.com/api-docs/endpoint/server-provider/region.html)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `organization` | path | `string` | yes |
| `cloudServerProvider` | path | `string` | yes |

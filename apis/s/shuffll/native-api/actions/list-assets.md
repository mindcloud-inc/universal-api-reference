# List Assets with Shuffll

Retrieves assets from Shuffll.

## Endpoint

- **Method:** `GET`
- **Path:** `/auth/organization/:organizationId/workspace/:workspaceId/assets`
- **Base URL:** `https://api.shuffll.com/api/v1`
- **Official documentation:** [List Assets](https://api-docs.shuffll.com/apis/assets/listassets)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `folder` | query | `string` | no | Optional folder filter. |
| `organizationId` | path | `string` | yes | Shuffll organization id. |
| `type` | query | `string` | no | Optional asset type filter. |
| `workspaceId` | path | `string` | yes | Shuffll workspace id. |

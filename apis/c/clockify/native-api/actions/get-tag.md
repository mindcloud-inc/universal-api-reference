# Get Tag with Clockify

Retrieves a specific tag from Clockify.

## Endpoint

- **Method:** `GET`
- **Path:** `workspaces/:workspaceId/tags/:id`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [Get Tag](https://docs.developer.clockify.me/#tag/Tag/operation/getTag)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspaceId` | path | `list<string>` | yes |
| `id` | path | `string<string>` | yes |

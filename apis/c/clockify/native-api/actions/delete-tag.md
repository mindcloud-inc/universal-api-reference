# Delete Tag with Clockify

Deletes an existing tag from Clockify.

## Endpoint

- **Method:** `DELETE`
- **Path:** `workspaces/:workspaceId/tags/:id`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [Delete Tag](https://docs.developer.clockify.me/#tag/Tag/operation/deleteTag)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspaceId` | path | `list<string>` | yes |
| `id` | path | `string<string>` | yes |

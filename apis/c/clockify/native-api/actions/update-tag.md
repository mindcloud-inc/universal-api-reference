# Update Tag with Clockify

Updates an existing tag in Clockify.

## Endpoint

- **Method:** `PUT`
- **Path:** `workspaces/:workspaceId/tags/:id`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [Update Tag](https://docs.developer.clockify.me/#tag/Tag/operation/updateTag)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceId` | path | `list<string>` | yes | — |
| `id` | path | `string<string>` | yes | — |
| `archived` | body | `boolean` | no | — |
| `name` | body | `string` | no | Maximum length: 100. |

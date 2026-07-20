# Create Workspace Tag with Clockify

Creates a new workspace tag in Clockify.

## Endpoint

- **Method:** `POST`
- **Path:** `workspaces/:workspaceId/tags`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [Create Workspace Tag](https://docs.developer.clockify.me/#tag/Tag/operation/createNewTag)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspaceId` | path | `list<string>` | yes |
| `name` | body | `string` | yes |

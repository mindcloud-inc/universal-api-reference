# List Workspace Tags with Clockify

Lists all workspace tags in Clockify.

## Endpoint

- **Method:** `GET`
- **Path:** `workspaces/:workspaceId/tags`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [List Workspace Tags](https://docs.developer.clockify.me/#tag/Tag/operation/getTags)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspaceId` | path | `list<string>` | yes |
| `name` | query | `string` | no |
| `strict-name-search` | query | `boolean` | no |
| `excluded-ids` | query | `string` | no |
| `archived` | query | `boolean` | no |

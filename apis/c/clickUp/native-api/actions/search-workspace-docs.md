# Search Workspace Docs with ClickUp

Finds Docs in a ClickUp Workspace.

## Endpoint

- **Method:** `GET`
- **Path:** `https://api.clickup.com/api/v3/workspaces/:workspace_id/docs`
- **Base URL:** `https://api.clickup.com/api/v2/`
- **Official documentation:** [Search Workspace Docs](https://developer.clickup.com/reference/searchdocspublic)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `archived` | query | `boolean` | no | Include archived docs filter |
| `creator` | query | `number` | no | Filter by creator user ID |
| `cursor` | query | `string` | no | Cursor for pagination |
| `deleted` | query | `boolean` | no | Include deleted docs filter |
| `id` | query | `string` | no | Filter by document ID |
| `limit` | query | `number` | no | Maximum number of docs to return |
| `next_cursor` | query | `string` | no | Forward pagination cursor |
| `parent_id` | query | `string` | no | Filter by parent entity ID |
| `parent_type` | query | `string` | no | Filter by parent entity type |
| `workspace_id` | path | `list` | yes | — |

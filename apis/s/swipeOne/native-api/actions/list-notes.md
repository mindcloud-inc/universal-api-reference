# List Notes with Swipe One

## Endpoint

- **Method:** `GET`
- **Path:** `/workspaces/:workspaceId/notes`
- **Base URL:** `https://api.swipeone.com/api`
- **Official documentation:** [List Notes](https://docs.swipeone.com/en/articles/10546101-notes#h_05759b3939)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceId` | path | `string` | yes | Workspace to list notes from. |
| `page` | query | `number` | no | Page number. |
| `limit` | query | `number` | no | Number of records per page. |
| `search` | query | `string` | no | Optional search term. |

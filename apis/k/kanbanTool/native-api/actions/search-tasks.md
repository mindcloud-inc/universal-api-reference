# Search Tasks with Kanban Tool

## Endpoint

- **Method:** `GET`
- **Path:** `/tasks/search.json`
- **Base URL:** `https://{domain}.kanbantool.com/api/v3`
- **Official documentation:** [Search Tasks](https://kanbantool.com/developer/api-v3#searching-tasks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | yes | Search query. Required by the API, but it may be an empty string. |
| `limit` | query | `number` | no | Maximum number of tasks to return, or tasks per page when `page` is also supplied. |
| `page` | query | `number` | no | Page number. When set, the API returns pagination metadata together with results. |
| `board_id` | query | `string` | no | Comma-separated list of board IDs to narrow the search scope. |
| `archived` | query | `number` | no | Set to `1` to search archived tasks. |

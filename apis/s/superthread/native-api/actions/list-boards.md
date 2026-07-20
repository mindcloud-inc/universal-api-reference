# List Boards with Superthread

## Endpoint

- **Method:** `GET`
- **Path:** `/:team_id/boards`
- **Base URL:** `https://api.superthread.com/v1`
- **Official documentation:** [List Boards](https://superthread.com/docs/api-docs/boards/get-boards)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `archived` | query | `boolean` | no | Return archived boards when enabled. |
| `bookmarked` | query | `boolean` | no | Return only bookmarked boards when enabled. |
| `project_id` | query | `string` | yes | Space ID used to scope boards. |
| `team_id` | path | `string` | yes | Workspace ID for the Superthread workspace. |

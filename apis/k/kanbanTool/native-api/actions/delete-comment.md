# Delete Comment with Kanban Tool

## Endpoint

- **Method:** `DELETE`
- **Path:** `/tasks/:task_id/comments/:comment_id.json`
- **Base URL:** `https://{domain}.kanbantool.com/api/v3`
- **Official documentation:** [Delete Comment](https://kanbantool.com/developer/api-v3#deleting-comments)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `task_id` | path | `number` | yes | Parent task ID. |
| `comment_id` | path | `number` | yes | Kanban Tool comment ID. |

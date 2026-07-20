# Create Comment with Kanban Tool

## Endpoint

- **Method:** `POST`
- **Path:** `/tasks/:task_id/comments.json`
- **Base URL:** `https://{domain}.kanbantool.com/api/v3`
- **Official documentation:** [Create Comment](https://kanbantool.com/developer/api-v3#creating-comments)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `task_id` | path | `number` | yes | Parent task ID. |
| `content` | body | `string` | yes | Comment body. |

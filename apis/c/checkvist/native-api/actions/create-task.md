# Create Task with Checkvist

Creates a task in Checkvist.

## Endpoint

- **Method:** `POST`
- **Path:** `/checklists/:checklistId/tasks.json`
- **Base URL:** `https://checkvist.com`
- **Official documentation:** [Create Task](https://checkvist.com/auth/api#list_items_create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `checklistId` | path | `number` | yes | The checklist ID. |
| `task.content` | body | `string` | yes | The task text. |
| `task.due_date` | body | `string` | no | A due date in Checkvist smart syntax. |
| `task.parent_id` | body | `string` | no | The parent task ID. |
| `task.position` | body | `number` | no | The 1-based position under the parent task. |
| `task.priority` | body | `number` | no | The task priority or color, from 0 to 9. |
| `task.status` | body | `string` | no | The optional task status. |
| `task.tags` | body | `string` | no | A comma-separated list of tags. |

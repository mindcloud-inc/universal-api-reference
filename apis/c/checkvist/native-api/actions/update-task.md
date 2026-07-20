# Update Task with Checkvist

Updates a task in Checkvist.

## Endpoint

- **Method:** `PUT`
- **Path:** `/checklists/:checklistId/tasks/:taskId.json`
- **Base URL:** `https://checkvist.com`
- **Official documentation:** [Update Task](https://checkvist.com/auth/api#list_items_update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `checklistId` | path | `number` | yes | The checklist ID. |
| `parse` | body | `boolean` | no | Recognize ^due and #tags syntax in the updated task. |
| `task.assignee_ids` | body | `string` | no | One or more task assignee IDs. |
| `task.content` | body | `string` | no | The updated task text. |
| `task.due_date` | body | `string` | no | A due date in Checkvist smart syntax. |
| `task.parent_id` | body | `string` | no | The new parent task ID. |
| `task.position` | body | `number` | no | The 1-based position under the parent task. |
| `task.priority` | body | `number` | no | The task priority or color, from 0 to 9. |
| `task.tags` | body | `string` | no | A comma-separated list of tags. |
| `taskId` | path | `number` | yes | The task ID. |
| `with_notes` | body | `boolean` | no | Include task notes in the response. |

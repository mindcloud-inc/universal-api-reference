# Update task with Pachca

## Endpoint

- **Method:** `PUT`
- **Path:** `/tasks/{id}`
- **Base URL:** `https://api.pachca.com/api/shared/v1`
- **Official documentation:** [Update task](https://dev.pachca.com/reference/tasks-id-update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Pachca task ID. |
| `task` | body | `object` | yes | Task parameters object. |
| `task.content` | body | `string` | no | Task description. |
| `task.status` | body | `string` | no | Task status. |
| `task.due_at` | body | `date` | no | Task due date in ISO-8601 format. |
| `task.priority` | body | `number` | no | Priority: 1, 2, or 3. |

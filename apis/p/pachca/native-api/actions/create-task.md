# Create task with Pachca

## Endpoint

- **Method:** `POST`
- **Path:** `/tasks`
- **Base URL:** `https://api.pachca.com/api/shared/v1`
- **Official documentation:** [Create task](https://dev.pachca.com/reference/tasks-create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `task` | body | `object` | yes | Task parameters object. |
| `task.kind` | body | `string` | yes | Task kind. Use reminder for reminders. |
| `task.content` | body | `string` | no | Task description. |
| `task.due_at` | body | `date` | no | Task due date in ISO-8601 format. |
| `task.priority` | body | `number` | no | Priority: 1, 2, or 3. |
| `task.performer_ids[]` | body | `array<number>` | no | User IDs assigned as task performers. Send multiple values as a array. |
| `task.chat_id` | body | `number` | no | Chat ID to link the task to. |
| `task.all_day` | body | `boolean` | no | Whether this is an all-day task. |

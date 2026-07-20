# Update Task with Kanban Tool

## Endpoint

- **Method:** `PATCH`
- **Path:** `/tasks/:task_id.json`
- **Base URL:** `https://{domain}.kanbantool.com/api/v3`
- **Official documentation:** [Update Task](https://kanbantool.com/developer/api-v3#updating-tasks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `task_id` | path | `number` | yes | Kanban Tool task ID. |
| `board_id` | body | `number` | no | Move the task to another board. |
| `name` | body | `string` | no | Task title. |
| `workflow_stage_id` | body | `number` | no | Target workflow stage. |
| `swimlane_id` | body | `number` | no | Target swimlane. |
| `card_type_id` | body | `number` | no | Card type to assign to the task. |
| `assigned_user_id` | body | `number` | no | User who should own the task. |
| `description` | body | `string` | no | Task description. HTML is supported. |
| `priority` | body | `number` | no | Task priority: `-1` low, `0` normal, `1` high. |
| `tags` | body | `string` | no | Comma-separated list of tags. |
| `time_estimate` | body | `number` | no | Estimated work in seconds. |
| `size_estimate` | body | `string` | no | Difficulty estimate string such as `1.0` or `5.0`. |
| `due_date` | body | `date` | no | Task due date. |
| `postponed_until` | body | `date` | no | Postpone the task until this date. |
| `position` | body | `number` | no | Task position inside the board cell. |
| `external_id` | body | `number` | no | Custom external identifier for synchronization. |
| `external_link` | body | `string` | no | Custom external URL for the task. |

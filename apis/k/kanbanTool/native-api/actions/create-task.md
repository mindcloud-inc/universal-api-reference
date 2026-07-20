# Create Task with Kanban Tool

## Endpoint

- **Method:** `POST`
- **Path:** `/tasks.json`
- **Base URL:** `https://{domain}.kanbantool.com/api/v3`
- **Official documentation:** [Create Task](https://kanbantool.com/developer/api-v3#creating-tasks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `board_id` | body | `number` | yes | Board where the task should be created. |
| `name` | body | `string` | yes | Task title. |
| `workflow_stage_id` | body | `number` | no | Workflow stage where the task should be created. |
| `swimlane_id` | body | `number` | no | Swimlane where the task should be created. |
| `card_type_id` | body | `number` | no | Card type to assign to the new task. |
| `assigned_user_id` | body | `number` | no | User who should own the task. |
| `description` | body | `string` | no | Task description. HTML is supported. |
| `priority` | body | `number` | no | Task priority: `-1` low, `0` normal, `1` high. |
| `tags` | body | `string` | no | Comma-separated list of tags. |
| `time_estimate` | body | `number` | no | Estimated work in seconds. |
| `size_estimate` | body | `string` | no | Difficulty estimate string such as `1.0` or `5.0`. |
| `due_date` | body | `date` | no | Task due date. |
| `postponed_until` | body | `date` | no | Postpone the task until this date. |
| `position` | body | `number` | no | Task position inside the target board cell. |
| `external_id` | body | `number` | no | Custom external identifier for synchronization. |
| `external_link` | body | `string` | no | Custom external URL for the task. |
| `task_attachment_ids` | body | `object` | no | JSON array of previously uploaded attachment IDs to attach to the new task. |
| `subtask_ids` | body | `object` | no | JSON array of existing subtask IDs to attach to the new task. |
| `assert_has_unique_external_id` | body | `boolean` | no | Fail when another task on the same board already uses the supplied external ID. |

# Update Subtask with Kanban Tool

## Endpoint

- **Method:** `PATCH`
- **Path:** `/subtasks/:subtask_id.json`
- **Base URL:** `https://{domain}.kanbantool.com/api/v3`
- **Official documentation:** [Update Subtask](https://kanbantool.com/developer/api-v3#updating-subtasks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `subtask_id` | path | `number` | yes | Kanban Tool subtask ID. |
| `name` | body | `string` | no | Subtask title. |
| `task_id` | body | `number` | no | Move the subtask to another task. |
| `assigned_user_id` | body | `number` | no | User who should own the subtask. |
| `is_completed` | body | `boolean` | no | Mark the subtask as completed. |

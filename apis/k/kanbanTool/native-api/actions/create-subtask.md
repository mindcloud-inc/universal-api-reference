# Create Subtask with Kanban Tool

## Endpoint

- **Method:** `POST`
- **Path:** `/subtasks.json`
- **Base URL:** `https://{domain}.kanbantool.com/api/v3`
- **Official documentation:** [Create Subtask](https://kanbantool.com/developer/api-v3#creating-subtasks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Subtask title. |
| `task_id` | body | `number` | yes | Parent task ID. |
| `assigned_user_id` | body | `number` | no | User who should own the subtask. |
| `is_completed` | body | `boolean` | no | Mark the subtask as completed immediately. |

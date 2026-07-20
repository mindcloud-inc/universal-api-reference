# Create Task with Freshworks CRM

Creates a new task in Freshworks CRM.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/tasks`
- **Base URL:** `https://{bundleAlias}`
- **Official documentation:** [Create Task](https://developers.freshworks.com/crm/api/#create_task)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `task` | body | `object` | yes | — |
| `task.description` | body | `string` | no | — |
| `task.due_date` | body | `string` | yes | Due date string for the task. Freshworks rejects task creation when due date is blank. |
| `task.owner_id` | body | `number` | no | — |
| `task.targetable_id` | body | `number` | yes | — |
| `task.targetable_type` | body | `string` | yes | — |
| `task.title` | body | `string` | yes | — |

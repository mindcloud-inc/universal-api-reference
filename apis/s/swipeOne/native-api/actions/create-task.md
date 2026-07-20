# Create Task with Swipe One

## Endpoint

- **Method:** `POST`
- **Path:** `/workspaces/:workspaceId/tasks`
- **Base URL:** `https://api.swipeone.com/api`
- **Official documentation:** [Create Task](https://docs.swipeone.com/en/articles/10546025-tasks#h_8e6a35db1f)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceId` | path | `string` | yes | The unique ID of the workspace where the task should be created. |
| `name` | body | `string` | yes | Name of the task. |
| `assignedTo` | body | `string` | no | The user assigned to the task. |
| `dueDate` | body | `date` | no | Due date of the task in ISO 8601 format. |
| `reminder` | body | `date` | no | Reminder date in ISO 8601 format. |
| `contactId` | body | `string` | no | The contact associated with the task. |

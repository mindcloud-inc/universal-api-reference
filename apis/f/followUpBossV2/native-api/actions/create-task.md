# Create Task with Follow Up Boss

Creates a new task in Follow Up Boss.

## Endpoint

- **Method:** `POST`
- **Path:** `tasks`
- **Base URL:** `https://api.followupboss.com/v1/`
- **Official documentation:** [Create Task](https://docs.followupboss.com/reference/tasks-post)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `personId` | body | `number` | no |
| `name` | body | `string` | no |
| `type` | body | `string` | no |
| `dueDate` | body | `date` | no |

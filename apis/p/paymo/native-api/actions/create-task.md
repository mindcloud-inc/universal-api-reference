# Create Task with Paymo

Creates a task in Paymo.

## Endpoint

- **Method:** `POST`
- **Path:** `tasks`
- **Base URL:** `https://app.paymoapp.com/api/`
- **Official documentation:** [Create Task](https://github.com/paymo-org/api/blob/master/sections/tasks.md#creating-a-task)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The task name. |
| `tasklist_id` | body | `number` | yes | The Paymo task list id the task belongs to. |
| `description` | body | `string` | no | Optional task description. |

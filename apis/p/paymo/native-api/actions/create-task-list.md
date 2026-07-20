# Create Task List with Paymo

Creates a task list in Paymo.

## Endpoint

- **Method:** `POST`
- **Path:** `tasklists`
- **Base URL:** `https://app.paymoapp.com/api/`
- **Official documentation:** [Create Task List](https://github.com/paymo-org/api/blob/master/sections/tasklists.md#creating-a-task-list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The task list name. |
| `project_id` | body | `number` | yes | The Paymo project id the task list belongs to. |

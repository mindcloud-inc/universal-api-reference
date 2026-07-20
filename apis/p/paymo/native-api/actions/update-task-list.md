# Update Task List with Paymo

Updates an existing task list in Paymo.

## Endpoint

- **Method:** `PUT`
- **Path:** `tasklists/:tasklistId`
- **Base URL:** `https://app.paymoapp.com/api/`
- **Official documentation:** [Update Task List](https://github.com/paymo-org/api/blob/master/sections/tasklists.md#updating-a-task-list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tasklistId` | path | `number` | yes | The Paymo task list id. |
| `name` | body | `string` | no | Updated task list name. |

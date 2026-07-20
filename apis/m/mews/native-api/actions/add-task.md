# Add Task with Mews

Creates a new task in Mews.

## Endpoint

- **Method:** `POST`
- **Path:** `/tasks/add`
- **Base URL:** `{platformAddress}/api/connector/v1`
- **Official documentation:** [Add Task](https://github.com/MewsSystems/gitbook-connector-api/blob/master/operations/tasks.md#add-task)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Name` | body | `string` | yes | Name or title of the task to create. |
| `DeadlineUtc` | body | `date` | yes | UTC deadline for the task. |

# Create Task with Nozbe Teams

Creates a new task in Nozbe Teams.

## Endpoint

- **Method:** `POST`
- **Path:** `/tasks`
- **Base URL:** `https://api4.nozbe.com/v1/api`
- **Official documentation:** [Create Task](https://api4.nozbe.com/v1/api#/tasks/postTask)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The task name. |
| `project_id` | body | `string` | yes | The project that will contain the task. |

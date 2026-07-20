# Create Task with Nozbe Personal

Creates a new task in Nozbe Personal.

## Endpoint

- **Method:** `POST`
- **Path:** `/tasks`
- **Base URL:** `https://api4.nozbe.com/v1/api`
- **Official documentation:** [Create Task](https://api4.nozbe.com/v1/api#/tasks/postTask)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Task name. |
| `project_id` | body | `string` | yes | Project ID for the task. |

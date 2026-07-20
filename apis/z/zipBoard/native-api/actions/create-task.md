# Create Task with zipBoard

Creates a new task in zipBoard.

## Endpoint

- **Method:** `POST`
- **Path:** `/issues/tasks`
- **Base URL:** `https://app.zipboard.co/api/v1`
- **Official documentation:** [Create Task](https://help.zipboard.co/article/181-api-for-issues-task)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | body | `string` | no | Optional task description. |
| `priority` | body | `string` | no | Optional task priority. |
| `projectid` | body | `string` | yes | Project ID where the task should be created. |
| `status` | body | `string` | no | Optional task status. |
| `title` | body | `string` | yes | Task title. |
| `type` | body | `string` | no | Optional task type. |

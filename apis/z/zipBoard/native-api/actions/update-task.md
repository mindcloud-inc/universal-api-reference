# Update Task with zipBoard

Updates an existing task in zipBoard.

## Endpoint

- **Method:** `PUT`
- **Path:** `/issues/tasks/:id`
- **Base URL:** `https://app.zipboard.co/api/v1`
- **Official documentation:** [Update Task](https://help.zipboard.co/article/181-api-for-issues-task)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | body | `string` | no | Updated task description. |
| `id` | path | `string` | yes | Task record ID to update. |
| `priority` | body | `string` | no | Updated task priority. |
| `status` | body | `string` | no | Updated task status. |
| `title` | body | `string` | no | Updated task title. |
| `type` | body | `string` | no | Updated task type. |

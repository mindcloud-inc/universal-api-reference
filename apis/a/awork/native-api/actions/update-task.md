# Update Task with Awork

Updates a task in Awork.

## Endpoint

- **Method:** `PUT`
- **Path:** `/tasks/:taskId`
- **Base URL:** `https://api.awork.com/api/v1`
- **Official documentation:** [Update Task](https://developers.awork.com/apiv1/tasks/put-task)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taskId` | path | `string` | yes | The id of the task. |
| `name` | body | `string` | yes | The name of the task. |
| `description` | body | `string` | no | The description of the task. |
| `isPrio` | body | `boolean` | no | Whether the task is marked as priority. |

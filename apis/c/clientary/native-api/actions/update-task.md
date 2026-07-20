# Update Task with Clientary

Updates a task in Clientary by task ID.

## Endpoint

- **Method:** `PUT`
- **Path:** `/tasks/:id`
- **Base URL:** `https://{subdomain}.clientary.com/api/v2`
- **Official documentation:** [Update Task](https://www.clientary.com/api/tasks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The Clientary task ID. |
| `task.complete` | body | `boolean` | no | Mark the task complete or incomplete. |

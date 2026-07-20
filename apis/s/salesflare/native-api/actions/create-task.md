# Create Task with Salesflare

## Endpoint

- **Method:** `POST`
- **Path:** `tasks`
- **Base URL:** `https://api.salesflare.com`
- **Official documentation:** [Create Task](https://api.salesflare.com/docs#/Tasks/postTasks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account` | body | `number` | no | The ID of the account linked to the task. |
| `description` | body | `string` | yes | The task description. |

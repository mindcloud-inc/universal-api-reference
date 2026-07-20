# List My Tasks with Chatwork

## Endpoint

- **Method:** `GET`
- **Path:** `/my/tasks`
- **Base URL:** `https://api.chatwork.com/v2`
- **Official documentation:** [List My Tasks](https://developer.chatwork.com/reference/get-my-tasks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `assigned_by_account_id` | query | `number` | no | Account ID of the user who assigned the task. |
| `status` | query | `list<string>` | no | Completion status of the task. Accepted values: `done`, `open`. |

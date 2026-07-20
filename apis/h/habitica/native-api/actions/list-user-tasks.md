# List User Tasks with Habitica

Retrieves the current user's tasks from Habitica.

## Endpoint

- **Method:** `GET`
- **Path:** `/tasks/user`
- **Base URL:** `https://habitica.com/api/v3`
- **Official documentation:** [List User Tasks](https://habitica.com/apidoc/#api-Task-GetUserTasks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `type` | query | `string` | no | Filter returned tasks to one Habitica task type. Accepted values: `0`, `1`, `2`, `3`. |

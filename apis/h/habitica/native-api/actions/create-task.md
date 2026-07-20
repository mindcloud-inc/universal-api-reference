# Create Task with Habitica

Creates a new task in Habitica.

## Endpoint

- **Method:** `POST`
- **Path:** `/tasks/user`
- **Base URL:** `https://habitica.com/api/v3`
- **Official documentation:** [Create Task](https://habitica.com/apidoc/#api-Task)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `text` | body | `string` | yes | The task title. |
| `type` | body | `string` | yes | The Habitica task type. Accepted values: `0`, `1`, `2`, `3`. |

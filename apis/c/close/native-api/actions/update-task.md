# Update Task with Close

Updates an existing task in Close.

## Endpoint

- **Method:** `PUT`
- **Path:** `/task/:id/`
- **Base URL:** `https://api.close.com/api/v1`
- **Official documentation:** [Update Task](https://developer.close.com/resources/tasks/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `date` | body | `date` | no | Task due date/time. |
| `id` | path | `string` | yes | Unique Task ID. |
| `is_complete` | body | `boolean` | no | Task completion state. |
| `text` | body | `string` | no | Task text. |

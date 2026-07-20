# Create Task with Close

Creates a new task in Close.

## Endpoint

- **Method:** `POST`
- **Path:** `/task/`
- **Base URL:** `https://api.close.com/api/v1`
- **Official documentation:** [Create Task](https://developer.close.com/resources/tasks/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `date` | body | `date` | no | Task due date/time. |
| `lead_id` | body | `string` | yes | Lead ID for this task. |
| `text` | body | `string` | yes | Task text. |

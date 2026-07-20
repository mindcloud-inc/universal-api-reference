# Edit Task with Datalyse

Updates an existing task in Datalyse.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/1.0/tasks/edit.json`
- **Base URL:** `https://api.datalyse.io`
- **Official documentation:** [Edit Task](https://developers.datalyse.io/devs/content_api.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `agent_id` | body | `string` | no | Agent ID or "unassigned" (optional) |
| `date` | body | `string` | no | Task date YYYY-MM-DD (optional) |
| `status` | body | `string` | no | Status ID (optional) |
| `subject` | body | `string` | no | Task subject (optional) |
| `task_id` | body | `string` | yes | ID of the task to edit |
| `text` | body | `string` | no | Task description (optional) |
| `time` | body | `string` | no | Task time HH:MM (optional) |

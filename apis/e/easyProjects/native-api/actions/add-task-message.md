# Add Task Message with Easy Projects

Creates a new message on an Easy Projects task.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/tasks/:id/messages`
- **Base URL:** `https://api.go.easyprojects.net/api/`
- **Official documentation:** [Add Task Message](https://api.go.easyprojects.net/api/v1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Birdview task ID. |
| `model` | body | `object` | yes | New task message model. |

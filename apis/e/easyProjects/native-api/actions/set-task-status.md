# Set Task Status with Easy Projects

Updates the status of an Easy Projects task.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/v1/tasks/:id/status`
- **Base URL:** `https://api.go.easyprojects.net/api/`
- **Official documentation:** [Set Task Status](https://api.go.easyprojects.net/api/v1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Birdview task ID. |
| `model` | body | `object` | yes | Task status update model. |

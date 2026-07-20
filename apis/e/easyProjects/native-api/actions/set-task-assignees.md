# Set Task Assignees with Easy Projects

Updates assignees for an Easy Projects task.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/v1/tasks/:id/assignees`
- **Base URL:** `https://api.go.easyprojects.net/api/`
- **Official documentation:** [Set Task Assignees](https://api.go.easyprojects.net/api/v1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Birdview task ID. |
| `model` | body | `object` | yes | Task assignee update model. |

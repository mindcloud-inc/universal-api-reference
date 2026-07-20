# Add Time Entry with Easy Projects

Creates a new time entry for an Easy Projects task.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/tasks/:id/time-entries`
- **Base URL:** `https://api.go.easyprojects.net/api/`
- **Official documentation:** [Add Time Entry](https://api.go.easyprojects.net/api/v1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Birdview task ID. |
| `model` | body | `object` | yes | New time entry model. |

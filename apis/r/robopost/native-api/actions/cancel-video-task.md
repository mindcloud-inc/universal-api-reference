# Cancel Video Task with Robopost

Deletes an existing video task from Robopost.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/video-tasks/{task_id}`
- **Base URL:** `https://public-api.robopost.app/v1`
- **Official documentation:** [Cancel Video Task](https://robopost.app/docs/robopost-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `task_id` | path | `string` | yes | The video task ID to cancel. |

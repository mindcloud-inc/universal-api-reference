# Complete Task with Podio

Marks an existing task complete in Podio.

## Endpoint

- **Method:** `POST`
- **Path:** `/task/:task_id/complete`
- **Base URL:** `https://api.podio.com`
- **Official documentation:** [Complete Task](https://developers.podio.com/doc/tasks/complete-task-22432)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `task_id` | path | `string` | yes | The ID of the task to complete. |
| `hook` | query | `boolean` | no | Run Podio hooks for the change. |
| `silent` | query | `boolean` | no | Suppress stream bumping and notifications for the completion. |

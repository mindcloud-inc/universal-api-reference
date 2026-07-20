# List Task Subtasks with Trackabi

Retrieves subtasks for a task from Trackabi.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/tasks/:taskId/subtasks`
- **Base URL:** `https://api.trackabi.com`
- **Official documentation:** [List Task Subtasks](https://trackabi.com/help/api-docs)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `task_id` | path | `number` | yes | The unique ID of the task. |

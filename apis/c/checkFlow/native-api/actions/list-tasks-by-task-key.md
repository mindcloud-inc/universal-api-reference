# List Tasks by Task Key with CheckFlow

## Endpoint

- **Method:** `GET`
- **Path:** `/api/checklist/tasks`
- **Base URL:** `https://app.checkflow.io`
- **Official documentation:** [List Tasks by Task Key](https://docs.checkflow.io/docs/api/checklists#get-tasks-by-task-key)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taskKey` | query | `string` | no | The key of the task to match. |
| `status` | query | `string` | no | Task status filter. |

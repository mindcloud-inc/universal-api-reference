# Delete Task with TickTick

Deletes an existing task from TickTick.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/open/v1/project/:projectId/task/:taskId`
- **Base URL:** `https://api.ticktick.com`
- **Official documentation:** [Delete Task](https://developer.ticktick.com/docs/index.html#/openapi?id=delete-task)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `list<string>` | yes | Project identifier |
| `taskId` | path | `string` | yes | Task identifier |

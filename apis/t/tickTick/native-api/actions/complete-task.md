# Complete Task with TickTick

Marks a task as complete in TickTick.

## Endpoint

- **Method:** `POST`
- **Path:** `/open/v1/project/:projectId/task/:taskId/complete`
- **Base URL:** `https://api.ticktick.com`
- **Official documentation:** [Complete Task](https://developer.ticktick.com/docs/index.html#/openapi?id=complete-task)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `list<string>` | yes | Project identifier |
| `taskId` | path | `string` | yes | Task identifier |

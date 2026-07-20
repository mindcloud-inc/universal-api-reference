# Get Task with TickTick

Retrieves a task from TickTick by project and task ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/open/v1/project/:projectId/task/:taskId`
- **Base URL:** `https://api.ticktick.com`
- **Official documentation:** [Get Task](https://developer.ticktick.com/docs/index.html#/openapi?id=get-task-by-project-id-and-task-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `list<string>` | yes | Project identifier |
| `taskId` | path | `string` | yes | Task identifier |

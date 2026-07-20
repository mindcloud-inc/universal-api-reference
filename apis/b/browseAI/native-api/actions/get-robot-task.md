# Get Robot Task with Browse AI

Retrieves a robot task from Browse AI.

## Endpoint

- **Method:** `GET`
- **Path:** `/robots/:robotId/tasks/:taskId`
- **Base URL:** `https://api.browse.ai/v2`
- **Official documentation:** [Get Robot Task](https://developers.browse.ai/v2#tag/tasks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `robotId` | path | `string` | yes | Unique robot ID  You can find a robot's ID by opening it on the dashboard and copying its ID in the browser address bar. |
| `taskId` | path | `string` | yes | Unique task ID |

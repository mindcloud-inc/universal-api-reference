# Get Project With Data with TickTick

Retrieves a project with its tasks and columns from TickTick.

## Endpoint

- **Method:** `GET`
- **Path:** `/open/v1/project/:projectId/data`
- **Base URL:** `https://api.ticktick.com`
- **Official documentation:** [Get Project With Data](https://developer.ticktick.com/docs/index.html#/openapi?id=get-project-with-data)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `list<string>` | yes | Project identifier |

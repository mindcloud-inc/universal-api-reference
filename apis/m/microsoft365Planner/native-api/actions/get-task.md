# Get Task with Microsoft 365 Planner

## Endpoint

- **Method:** `GET`
- **Path:** `/v1.0/planner/tasks/{{taskId}}`
- **Base URL:** `https://graph.microsoft.com`
- **Official documentation:** [Get Task](https://learn.microsoft.com/en-us/graph/api/plannertask-get?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taskId` | path | `string` | yes | Planner task ID to retrieve. |

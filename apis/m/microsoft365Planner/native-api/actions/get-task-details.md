# Get Task Details with Microsoft 365 Planner

## Endpoint

- **Method:** `GET`
- **Path:** `/v1.0/planner/tasks/{{taskId}}/details`
- **Base URL:** `https://graph.microsoft.com`
- **Official documentation:** [Get Task Details](https://learn.microsoft.com/en-us/graph/api/plannertaskdetails-get?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taskId` | path | `string` | yes | Planner task ID whose details should be retrieved. |

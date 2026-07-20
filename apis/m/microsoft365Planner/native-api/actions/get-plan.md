# Get Plan with Microsoft 365 Planner

## Endpoint

- **Method:** `GET`
- **Path:** `/v1.0/planner/plans/{{planId}}`
- **Base URL:** `https://graph.microsoft.com`
- **Official documentation:** [Get Plan](https://learn.microsoft.com/en-us/graph/api/plannerplan-get?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `planId` | path | `string` | yes | Planner plan ID to retrieve. |

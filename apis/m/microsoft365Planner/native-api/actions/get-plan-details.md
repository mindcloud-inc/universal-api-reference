# Get Plan Details with Microsoft 365 Planner

## Endpoint

- **Method:** `GET`
- **Path:** `/v1.0/planner/plans/{{planId}}/details`
- **Base URL:** `https://graph.microsoft.com`
- **Official documentation:** [Get Plan Details](https://learn.microsoft.com/en-us/graph/api/plannerplandetails-get?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `planId` | path | `string` | yes | Planner plan ID whose details should be retrieved. |

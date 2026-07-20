# List Plan Buckets with Microsoft 365 Planner

## Endpoint

- **Method:** `GET`
- **Path:** `/v1.0/planner/plans/{{planId}}/buckets`
- **Base URL:** `https://graph.microsoft.com`
- **Official documentation:** [List Plan Buckets](https://learn.microsoft.com/en-us/graph/api/plannerplan-list-buckets?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `planId` | path | `string` | yes | Planner plan ID whose buckets should be listed. |

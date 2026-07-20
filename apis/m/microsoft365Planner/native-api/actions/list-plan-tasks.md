# List Plan Tasks with Microsoft 365 Planner

## Endpoint

- **Method:** `GET`
- **Path:** `/v1.0/planner/plans/{{planId}}/tasks`
- **Base URL:** `https://graph.microsoft.com`
- **Official documentation:** [List Plan Tasks](https://learn.microsoft.com/en-us/graph/api/plannerplan-list-tasks?view=graph-rest-1.0)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `planId` | path | `string` | yes | Planner plan ID whose tasks should be listed. |

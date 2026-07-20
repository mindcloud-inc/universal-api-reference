# List Group Plans with Microsoft 365 Planner

## Endpoint

- **Method:** `GET`
- **Path:** `/v1.0/groups/{{groupId}}/planner/plans`
- **Base URL:** `https://graph.microsoft.com`
- **Official documentation:** [List Group Plans](https://learn.microsoft.com/en-us/graph/api/plannergroup-list-plans?view=graph-rest-1.0)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | path | `string` | yes | Microsoft 365 group ID whose Planner plans should be listed. |

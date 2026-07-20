# List Groups with Microsoft 365 Planner

## Endpoint

- **Method:** `GET`
- **Path:** `/v1.0/groups`
- **Base URL:** `https://graph.microsoft.com`
- **Official documentation:** [List Groups](https://learn.microsoft.com/en-us/graph/api/group-list?view=graph-rest-1.0)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `$filter` | query | `string` | no | Optional OData filter for groups, such as groupTypes/any(c:c eq 'Unified') for Microsoft 365 groups. |

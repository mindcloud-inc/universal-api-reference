# Create Plan with Microsoft 365 Planner

## Endpoint

- **Method:** `POST`
- **Path:** `/v1.0/planner/plans`
- **Base URL:** `https://graph.microsoft.com`
- **Official documentation:** [Create Plan](https://learn.microsoft.com/en-us/graph/api/planner-post-plans?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | yes | Title for the new Planner plan. |
| `container.url` | body | `string` | yes | Microsoft Graph URL for the plan container, such as https://graph.microsoft.com/v1.0/groups/{group-id}. |

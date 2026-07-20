# Delete Route with Zeo Route Planner

Deletes an existing route from Zeo Route Planner.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/v5/routes/:route_id`
- **Base URL:** `https://zeorouteplanner.com`
- **Official documentation:** [Delete Route](https://api.zeorouteplanner.com/delete-route.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `driver_id` | query | `number` | yes | Driver Id of the route. |
| `route_id` | path | `number` | yes | Route id we get from route list. |

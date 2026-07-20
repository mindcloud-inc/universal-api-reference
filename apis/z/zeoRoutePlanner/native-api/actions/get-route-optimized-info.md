# Get Route Optimized Info with Zeo Route Planner

Retrieves optimized route details from Zeo Route Planner.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v5/routes/:route_id/optimize_route`
- **Base URL:** `https://zeorouteplanner.com`
- **Official documentation:** [Get Route Optimized Info](https://api.zeorouteplanner.com/get-route-optimize-info.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `driver_id` | query | `number` | yes | Driver id of the route. |
| `route_id` | path | `number` | yes | Route id to fetch optimized information for. |

# Get Pickup Delivery Route Optimized Info with Zeo Route Planner

Retrieves optimized pickup delivery route details from Zeo Route Planner.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v6/routes/:route_id/optimize_route`
- **Base URL:** `https://zeorouteplanner.com`
- **Official documentation:** [Get Pickup Delivery Route Optimized Info](https://api.zeorouteplanner.com/pickup-delivery-get-route-optimized-info.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `driver_id` | query | `number` | yes | Driver id of the pickup delivery route. |
| `route_id` | path | `number` | yes | Pickup delivery route id. |

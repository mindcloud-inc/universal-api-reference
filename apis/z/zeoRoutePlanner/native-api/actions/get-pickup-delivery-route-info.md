# Get Pickup Delivery Route Info with Zeo Route Planner

Retrieves pickup delivery route details from Zeo Route Planner.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v6/routes/:route_id`
- **Base URL:** `https://zeorouteplanner.com`
- **Official documentation:** [Get Pickup Delivery Route Info](https://api.zeorouteplanner.com/pickup-deliver-get-route-info.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `driver_id` | query | `number` | yes | Driver id of the pickup delivery route. |
| `route_id` | path | `number` | yes | Pickup delivery route id. |

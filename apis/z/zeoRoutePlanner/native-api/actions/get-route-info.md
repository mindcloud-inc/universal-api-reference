# Get Route Info with Zeo Route Planner

Retrieves route details from Zeo Route Planner.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v5/routes/:route_id`
- **Base URL:** `https://zeorouteplanner.com`
- **Official documentation:** [Get Route Info](https://api.zeorouteplanner.com/get-route-info.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `driver_id` | query | `number` | yes | Driver identifier for the route. |
| `route_id` | path | `number` | yes | Route identifier. |

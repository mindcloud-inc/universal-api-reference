# Delete Pickup Delivery Route with Zeo Route Planner

Deletes a pickup delivery route from Zeo Route Planner.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/v6/routes/:route_id`
- **Base URL:** `https://zeorouteplanner.com`
- **Official documentation:** [Delete Pickup Delivery Route](https://api.zeorouteplanner.com/delete-pickup-delivery-route.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `driver_id` | query | `number` | yes | Driver id of the pickup delivery route. |
| `route_id` | path | `number` | yes | Pickup delivery route id. |

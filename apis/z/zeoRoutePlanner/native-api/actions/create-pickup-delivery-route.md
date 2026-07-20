# Create Pickup Delivery Route with Zeo Route Planner

Creates a pickup delivery route in Zeo Route Planner.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v6/routes`
- **Base URL:** `https://zeorouteplanner.com`
- **Official documentation:** [Create Pickup Delivery Route](https://api.zeorouteplanner.com/pickup-deliver-create-route.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `driver_id` | body | `number` | yes | Driver id for the pickup delivery route. |
| `end_address` | body | `string` | yes | Route end address. |
| `end_latitude` | body | `number` | yes | End latitude when provided. |
| `end_longitude` | body | `number` | yes | End longitude when provided. |
| `route_name` | body | `string` | yes | Route name. |
| `start_address` | body | `string` | yes | Address where the route starts. |
| `start_latitude` | body | `number` | yes | Starting latitude when provided. |
| `start_longitude` | body | `number` | yes | Starting longitude when provided. |
| `stops[]` | body | `array<object>` | yes | Pickup and delivery stops as an array of objects. |

# Create Route with Zeo Route Planner

Creates a new route in Zeo Route Planner.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v5/routes`
- **Base URL:** `https://zeorouteplanner.com`
- **Official documentation:** [Create Route](https://api.zeorouteplanner.com/create-route.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `driver_id` | body | `number` | yes | Driver id to assign the route. |
| `end_address` | body | `string` | yes | Route end address. |
| `end_latitude` | body | `number` | yes | End address latitude. |
| `end_longitude` | body | `number` | yes | End address longitude. |
| `orginal` | body | `boolean` | no | Original route generation flag. |
| `route_date` | body | `string` | no | Route date. |
| `route_name` | body | `string` | yes | Name of the route. |
| `start_address` | body | `string` | yes | Route start address. |
| `start_latitude` | body | `number` | yes | Start address latitude. |
| `start_longitude` | body | `number` | yes | Start address longitude. |
| `stops[]` | body | `array<object>` | yes | Stops between route start and end as an array of objects. |

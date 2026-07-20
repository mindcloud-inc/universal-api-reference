# Create Stops with Zeo Route Planner

Creates stops in Zeo Route Planner.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v5/route_stop`
- **Base URL:** `https://zeorouteplanner.com`
- **Official documentation:** [Create Stops](https://api.zeorouteplanner.com/create-stops.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `stops[]` | body | `array<object>` | yes | Stops to create as an array of stop objects. |

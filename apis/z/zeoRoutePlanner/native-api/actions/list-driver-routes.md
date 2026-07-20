# List Driver Routes with Zeo Route Planner

Retrieves routes for a driver in Zeo Route Planner.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v5/routes`
- **Base URL:** `https://zeorouteplanner.com`
- **Official documentation:** [List Driver Routes](https://api.zeorouteplanner.com/get-all-driver-routes.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `driver_id` | query | `number` | yes | Driver id whose routes to list. |
| `limit` | query | `number` | no | Records to return. |
| `offset` | query | `number` | no | Next records to return. |

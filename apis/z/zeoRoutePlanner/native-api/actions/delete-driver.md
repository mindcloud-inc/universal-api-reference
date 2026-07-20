# Delete Driver with Zeo Route Planner

Deletes an existing driver from Zeo Route Planner.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/v5/drivers/:driver_id`
- **Base URL:** `https://zeorouteplanner.com`
- **Official documentation:** [Delete Driver](https://api.zeorouteplanner.com/delete-driver.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `driver_id` | path | `number` | yes | Driver id we get from all driver APIs. |

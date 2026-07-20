# Remove Dashboard with Better Stack Telemetry

Deletes an existing dashboard from Better Stack Telemetry.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/v2/dashboards/:id`
- **Base URL:** `https://telemetry.betterstack.com`
- **Official documentation:** [Remove Dashboard](https://betterstack.com/docs/logs/api/dashboards/delete/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The unique identifier of the dashboard to delete. |

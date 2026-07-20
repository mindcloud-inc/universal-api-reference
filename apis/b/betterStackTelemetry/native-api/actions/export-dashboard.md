# Export Dashboard with Better Stack Telemetry

Exports a dashboard from Better Stack Telemetry.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/dashboards/:id/export`
- **Base URL:** `https://telemetry.betterstack.com`
- **Official documentation:** [Export Dashboard](https://betterstack.com/docs/logs/api/dashboards/export/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The unique identifier of the dashboard or template to export. |

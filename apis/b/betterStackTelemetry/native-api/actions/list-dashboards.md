# List Dashboards with Better Stack Telemetry

Retrieves dashboards from Better Stack Telemetry.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/dashboards`
- **Base URL:** `https://telemetry.betterstack.com`
- **Official documentation:** [List Dashboards](https://betterstack.com/docs/logs/api/dashboards/list/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `number` | no | Page number for pagination. |
| `per_page` | query | `number` | no | Number of items per page (max 250). |

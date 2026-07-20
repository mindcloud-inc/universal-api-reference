# Import Dashboard with Better Stack Telemetry

Imports a dashboard into Better Stack Telemetry.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/dashboards/import`
- **Base URL:** `https://telemetry.betterstack.com`
- **Official documentation:** [Import Dashboard](https://betterstack.com/docs/logs/api/dashboards/import/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | A name for the new dashboard. |
| `data` | body | `object` | yes | The dashboard configuration data in JSON format, typically obtained from the Export Dashboard endpoint. |
| `team_name` | body | `string` | no | Required if using a global API token to specify the team which should own the resource. |

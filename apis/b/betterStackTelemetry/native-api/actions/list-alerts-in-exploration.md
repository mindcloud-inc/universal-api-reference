# List Alerts In Exploration with Better Stack Telemetry

Retrieves alerts in an exploration from Better Stack Telemetry.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/explorations/:exploration_id/alerts`
- **Base URL:** `https://telemetry.betterstack.com`
- **Official documentation:** [List Alerts In Exploration](https://betterstack.com/docs/logs/api/alerts/list/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `exploration_id` | path | `string` | yes | The ID of the exploration whose alerts to list. |

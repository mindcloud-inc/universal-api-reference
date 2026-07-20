# Cancel Downtime with Datadog

Cancels an existing downtime in Datadog.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/v2/downtime/:downtime_id`
- **Base URL:** `https://api.us5.datadoghq.com`
- **Official documentation:** [Cancel Downtime](https://docs.datadoghq.com/api/latest/downtimes/#cancel-a-downtime)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `downtime_id` | path | `string` | yes | The ID of the downtime. |

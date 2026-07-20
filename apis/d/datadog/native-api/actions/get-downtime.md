# Get Downtime with Datadog

Retrieves a downtime from Datadog.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/downtime/:downtime_id`
- **Base URL:** `https://api.us5.datadoghq.com`
- **Official documentation:** [Get Downtime](https://docs.datadoghq.com/api/latest/downtimes/#get-a-downtime)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `downtime_id` | path | `string` | yes | The ID of the downtime. |
| `include` | query | `string` | no | Additional related resources to include. |

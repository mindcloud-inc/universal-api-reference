# Schedule Downtime with Datadog

Creates a new downtime in Datadog.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/downtime`
- **Base URL:** `https://api.us5.datadoghq.com`
- **Official documentation:** [Schedule Downtime](https://docs.datadoghq.com/api/latest/downtimes/#schedule-a-downtime)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data` | body | `object` | yes | JSON:API downtime payload. |

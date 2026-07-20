# List Active Metrics with Datadog

Retrieves active metrics from Datadog.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/metrics`
- **Base URL:** `https://api.us5.datadoghq.com`
- **Official documentation:** [List Active Metrics](https://docs.datadoghq.com/api/latest/metrics/#get-active-metrics-list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from` | query | `number` | yes | Seconds since the Unix epoch. |
| `host` | query | `string` | no | Hostname for filtering the metrics returned. |
| `tag_filter` | query | `string` | no | Filter metrics using tag expressions. |

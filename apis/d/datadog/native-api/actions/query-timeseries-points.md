# Query Timeseries Points with Datadog

Retrieves timeseries points from Datadog.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/query`
- **Base URL:** `https://api.us5.datadoghq.com`
- **Official documentation:** [Query Timeseries Points](https://docs.datadoghq.com/api/latest/metrics/#query-timeseries-points)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from` | query | `number` | yes | Start of the queried time period in epoch seconds. |
| `to` | query | `number` | yes | End of the queried time period in epoch seconds. |
| `query` | query | `string` | yes | Metrics query string. |

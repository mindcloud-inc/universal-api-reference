# Retrieve aggregated metrics with api.video

Retrieves aggregated analytics metrics from api.video.

## Endpoint

- **Method:** `GET`
- **Path:** `/data/metrics/:metric/:aggregation`
- **Base URL:** `https://ws.api.video`
- **Official documentation:** [Retrieve aggregated metrics](https://docs.api.video/reference/api/Analytics#retrieve-aggregated-metrics)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `aggregation` | path | `string` | yes | The aggregation to apply to the metric. |
| `metric` | path | `string` | yes | The metric to retrieve. |

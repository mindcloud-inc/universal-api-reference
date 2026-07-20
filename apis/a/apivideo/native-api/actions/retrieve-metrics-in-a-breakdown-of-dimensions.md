# Retrieve metrics in a breakdown of dimensions with api.video

Retrieves analytics metrics by dimension from api.video.

## Endpoint

- **Method:** `GET`
- **Path:** `/data/buckets/:metric/:breakdown`
- **Base URL:** `https://ws.api.video`
- **Official documentation:** [Retrieve metrics in a breakdown of dimensions](https://docs.api.video/reference/api/Analytics#retrieve-metrics-in-a-breakdown-of-dimensions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `breakdown` | path | `string` | yes | The dimension breakdown to apply to the metric. |
| `metric` | path | `string` | yes | The metric to retrieve. |

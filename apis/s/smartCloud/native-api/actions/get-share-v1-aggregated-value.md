# Aggregated value for topic with 2Smart Cloud

## Endpoint

- **Method:** `GET`
- **Path:** `/share/v1/aggregated-value`
- **Base URL:** `https://cloud.2smart.com/robot/v1`
- **Official documentation:** [Aggregated value for topic](https://cloud.2smart.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `topic` | query | `string` | yes | Metric topic in broker |
| `period` | query | `string` | yes | — |
| `aggregator` | query | `string` | yes | — |
| `fromTime` | query | `string` | no | Starting from datetime YYYY-MM-DDTHH:MM:SSZ (RFC3339) |
| `toTime` | query | `string` | no | Till datetime YYYY-MM-DDTHH:MM:SSZ (RFC3339) |

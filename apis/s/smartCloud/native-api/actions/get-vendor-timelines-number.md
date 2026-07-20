# List timelines number with 2Smart Cloud

## Endpoint

- **Method:** `GET`
- **Path:** `/vendor/timelines/number`
- **Base URL:** `https://cloud.2smart.com/robot/v1`
- **Official documentation:** [List timelines number](https://cloud.2smart.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `topic` | query | `string` | yes | Metric topic in broker |
| `period` | query | `string` | yes | — |
| `interval` | query | `string` | yes | — |
| `limit` | query | `number` | no | The number of rows to return |
| `offset` | query | `number` | no | Pagination offset |
| `fromTime` | query | `date` | no | Starting from datetime YYYY-MM-DDTHH:MM:SSZ (RFC3339) |
| `toTime` | query | `date` | no | Till datetime YYYY-MM-DDTHH:MM:SSZ (RFC3339) |

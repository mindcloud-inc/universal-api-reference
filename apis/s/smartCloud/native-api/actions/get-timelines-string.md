# List timelines string with 2Smart Cloud

## Endpoint

- **Method:** `GET`
- **Path:** `/timelines/string`
- **Base URL:** `https://cloud.2smart.com/robot/v1`
- **Official documentation:** [List timelines string](https://cloud.2smart.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `topic` | query | `string` | yes | Metric topic in broker |
| `period` | query | `string` | yes | Requested period |
| `interval` | query | `string` | yes | Requested interval |
| `limit` | query | `number` | no | The number of rows to return |
| `offset` | query | `number` | no | Pagination offset |
| `fromTime` | query | `date` | no | Starting from datetime YYYY-MM-DDTHH:MM:SSZ (RFC3339) |
| `toTime` | query | `date` | no | Till datetime YYYY-MM-DDTHH:MM:SSZ (RFC3339) |

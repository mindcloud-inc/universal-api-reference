# List share timelines number with 2Smart Cloud

## Endpoint

- **Method:** `GET`
- **Path:** `/share/v1/timelines/number`
- **Base URL:** `https://cloud.2smart.com/robot/v1`
- **Official documentation:** [List share timelines number](https://cloud.2smart.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `token` | query | `string` | yes | Share token used in request header |
| `topic` | query | `string` | yes | Metric topic in broker |
| `period` | query | `string` | yes | Requested period |
| `interval` | query | `string` | yes | Requested interval |
| `fromTime` | query | `date` | no | Starting from datetime YYYY-MM-DDTHH:MM:SSZ (RFC3339) |
| `toTime` | query | `date` | no | Till datetime YYYY-MM-DDTHH:MM:SSZ (RFC3339) |

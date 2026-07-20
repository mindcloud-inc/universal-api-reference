# List Monitor Events with Parallel Web Systems

## Endpoint

- **Method:** `GET`
- **Path:** `/v1alpha/monitors/:monitor_id/events`
- **Base URL:** `https://api.parallel.ai`
- **Official documentation:** [List Monitor Events](https://docs.parallel.ai/api-reference/monitor/list-events)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `monitor_id` | path | `string` | yes | The Parallel monitor ID. |
| `lookback_period` | query | `string` | no | Lookback period to fetch events from, such as 10d or 1w. |

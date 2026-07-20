# View Heartbeat Statistics with Pinghome

Retrieves heartbeat statistics from Pinghome.

## Endpoint

- **Method:** `GET`
- **Path:** `/statistic-query/v1/heartbeat/:id/statistic`
- **Base URL:** `https://api.pinghome.io`
- **Official documentation:** [View Heartbeat Statistics](https://docs.pinghome.io/monitoring/heartbeat-monitoring/view-heartbeat-statistics/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The unique ID of the heartbeat monitor. |
| `interval` | query | `string` | no | Defines the interval for retrieving statistics. |
| `start_date` | query | `string` | no | Start date for retrieving statistics. |
| `end_date` | query | `string` | no | End date for retrieving statistics. |

# View Uptime Monitor Performance Report with Pinghome

Retrieves an uptime monitor performance report from Pinghome.

## Endpoint

- **Method:** `GET`
- **Path:** `/statistic-query/v1/resource/:id/statistic`
- **Base URL:** `https://api.pinghome.io`
- **Official documentation:** [View Uptime Monitor Performance Report](https://docs.pinghome.io/monitoring/uptime-monitoring/view-uptime-monitor-performance-report/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The unique ID of the resource for which statistics are being retrieved. |
| `start_date` | query | `string` | no | Specifies the start date for retrieving statistics if needed. |
| `end_date` | query | `string` | no | Specifies the end date for retrieving statistics if needed. |
| `interval` | query | `string` | no | The aggregation interval for the report. |
| `limit` | query | `number` | no | The maximum number of data points to return. |

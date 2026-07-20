# View Uptime Monitor Response Log History with Pinghome

Retrieves uptime monitor response log history from Pinghome.

## Endpoint

- **Method:** `GET`
- **Path:** `/response-manager/v1/resource/:id/responses`
- **Base URL:** `https://api.pinghome.io`
- **Official documentation:** [View Uptime Monitor Response Log History](https://docs.pinghome.io/monitoring/uptime-monitoring/view-uptime-monitor-response-log-history/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The unique ID of the uptime monitor. |
| `start_date` | query | `string` | no | Start date to retrieve logs from. |
| `end_date` | query | `string` | no | End date to retrieve logs until. |
| `limit` | query | `number` | no | The maximum number of response log entries to return. |

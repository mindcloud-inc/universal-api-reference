# View Uptime Monitor State Change History with Pinghome

Retrieves uptime monitor state change history from Pinghome.

## Endpoint

- **Method:** `GET`
- **Path:** `/statistic-query/v1/resource/:id/state-changed-logs`
- **Base URL:** `https://api.pinghome.io`
- **Official documentation:** [View Uptime Monitor State Change History](https://docs.pinghome.io/monitoring/uptime-monitoring/view-uptime-monitor-state-change-history/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The unique ID of the uptime monitor. |
| `start_date` | query | `string` | no | Start date to retrieve logs from. |
| `end_date` | query | `string` | no | End date to retrieve logs until. |
| `limit` | query | `number` | no | The maximum number of log entries to return. |

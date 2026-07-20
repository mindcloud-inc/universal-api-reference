# Get Monitor Availability Summary with Better Stack Uptime

Retrieves an availability summary for a monitor in Better Stack Uptime.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/monitors/:monitor_id/sla`
- **Base URL:** `https://uptime.betterstack.com/api`
- **Official documentation:** [Get Monitor Availability Summary](https://betterstack.com/docs/uptime/api/get-a-monitors-availability-summary/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `monitor_id` | path | `string` | yes | The ID of the monitor you want to get availability for |
| `from` | query | `string` | no | Start date in YYYY-MM-DD format |
| `to` | query | `string` | no | End date in YYYY-MM-DD format |

# Get Heartbeat Availability Summary with Better Stack Uptime

Retrieves an availability summary for a heartbeat in Better Stack Uptime.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/heartbeats/:heartbeat_id/availability`
- **Base URL:** `https://uptime.betterstack.com/api`
- **Official documentation:** [Get Heartbeat Availability Summary](https://betterstack.com/docs/uptime/api/get-a-heartbeats-availability-summary/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `heartbeat_id` | path | `string` | yes | The heartbeat ID. |
| `from` | query | `string` | no | The start date for the availability summary. |
| `to` | query | `string` | no | The end date for the availability summary. |

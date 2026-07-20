# Get Monitor Response Times with Better Stack Uptime

Retrieves response times for a monitor in Better Stack Uptime.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/monitors/:monitor_id/response-times`
- **Base URL:** `https://uptime.betterstack.com/api`
- **Official documentation:** [Get Monitor Response Times](https://betterstack.com/docs/uptime/api/get-monitors-response-times/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `monitor_id` | path | `string` | yes | The ID of the monitor you want to get response times for |

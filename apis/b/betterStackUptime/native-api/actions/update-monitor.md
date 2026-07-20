# Update Monitor with Better Stack Uptime

Updates an existing monitor in Better Stack Uptime.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v2/monitors/:monitor_id`
- **Base URL:** `https://uptime.betterstack.com/api`
- **Official documentation:** [Update Monitor](https://betterstack.com/docs/uptime/api/update-an-existing-monitor/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `monitor_id` | path | `string` | yes | The ID of the monitor you want to update |
| `pronounceable_name` | body | `string` | no | The name of the monitor |
| `email` | body | `boolean` | no | Send email alerts |
| `sms` | body | `boolean` | no | Send SMS alerts |
| `call` | body | `boolean` | no | Phone call alerts |
| `push` | body | `boolean` | no | Should we send a push notification to the on-call person? |
| `critical_alert` | body | `boolean` | no | Send a critical alert to the on-call person |
| `check_frequency` | body | `number` | no | Check frequency in seconds |
| `paused` | body | `boolean` | no | Set to true to pause monitoring |
| `verify_ssl` | body | `boolean` | no | Whether to verify SSL certificates |

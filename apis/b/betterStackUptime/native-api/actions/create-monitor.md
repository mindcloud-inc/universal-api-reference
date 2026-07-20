# Create Monitor with Better Stack Uptime

Creates a new monitor in Better Stack Uptime.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/monitors`
- **Base URL:** `https://uptime.betterstack.com/api`
- **Official documentation:** [Create Monitor](https://betterstack.com/docs/uptime/api/create-a-new-monitor/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `monitor_type` | body | `string` | yes | Valid monitor type from Better Stack, such as status or expected_status_code |
| `url` | body | `string` | yes | The URL of your website or the host you want to ping |
| `pronounceable_name` | body | `string` | yes | The name of the monitor |
| `email` | body | `boolean` | no | Send email alerts |
| `sms` | body | `boolean` | no | Send SMS alerts |
| `call` | body | `boolean` | no | Phone call alerts |
| `critical_alert` | body | `boolean` | no | Send a critical alert to the on-call person |
| `check_frequency` | body | `number` | no | Check frequency in seconds |
| `paused` | body | `boolean` | no | Set to true to pause monitoring |
| `verify_ssl` | body | `boolean` | no | Whether to verify SSL certificates |
| `push` | body | `boolean` | no | Should we send a push notification to the on-call person? |

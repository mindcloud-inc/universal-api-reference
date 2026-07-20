# Create Uptime Monitor with Pinghome

Creates a new uptime monitor in Pinghome.

## Endpoint

- **Method:** `POST`
- **Path:** `/resource-cmd/v1/resource`
- **Base URL:** `https://api.pinghome.io`
- **Official documentation:** [Create Uptime Monitor](https://docs.pinghome.io/monitoring/uptime-monitoring/create-uptime-monitor/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `grace_period` | body | `number` | yes | Grace period before an incident is triggered. |
| `is_advanced` | body | `boolean` | yes | Whether advanced monitoring mode is enabled. |
| `method` | body | `string` | yes | The HTTP method used for the monitor request. |
| `name` | body | `string` | yes | The name of the uptime monitor. |
| `not_follow_redirect` | body | `boolean` | yes | Whether redirects should not be followed. |
| `recovery_period` | body | `number` | yes | Recovery period before the monitor is considered healthy again. |
| `regions[]` | body | `array<string>` | yes | The AWS regions that should run checks for this monitor. |
| `service_id` | body | `string` | yes | The service id that owns the uptime monitor. |
| `skip_ssl_error` | body | `boolean` | yes | Whether SSL certificate errors should be ignored. |
| `type` | body | `string` | yes | The monitor protocol type, such as http. |
| `url` | body | `string` | yes | The URL to monitor. |

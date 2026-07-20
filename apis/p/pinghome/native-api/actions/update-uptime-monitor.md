# Update Uptime Monitor with Pinghome

Updates an existing uptime monitor in Pinghome.

## Endpoint

- **Method:** `PUT`
- **Path:** `/resource-cmd/v1/resource/:id`
- **Base URL:** `https://api.pinghome.io`
- **Official documentation:** [Update Uptime Monitor](https://docs.pinghome.io/monitoring/uptime-monitoring/update-uptime-monitor/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The unique ID of the uptime monitor. |
| `name` | body | `string` | yes | The name of the uptime resource. |
| `is_advanced` | body | `boolean` | no | Whether the resource uses advanced monitoring options. |
| `method` | body | `string` | yes | The HTTP method used for uptime checks. |
| `grace_period` | body | `number` | no | Grace period before considering a failure. |
| `recovery_period` | body | `number` | no | Recovery period before considering the resource recovered. |
| `skip_ssl_error` | body | `boolean` | no | Whether SSL errors should be skipped. |
| `not_follow_redirect` | body | `boolean` | no | Whether redirects should not be followed. |
| `service_id` | body | `string` | yes | The service associated with the monitor. |
| `url` | body | `string` | yes | The target URL to monitor. |
| `regions[]` | body | `array<string>` | yes | Regions used to run the uptime checks. |

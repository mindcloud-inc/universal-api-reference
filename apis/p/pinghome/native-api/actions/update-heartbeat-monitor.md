# Update Heartbeat Monitor with Pinghome

Updates an existing heartbeat monitor in Pinghome.

## Endpoint

- **Method:** `PUT`
- **Path:** `/resource-cmd/v1/heartbeat/:id`
- **Base URL:** `https://api.pinghome.io`
- **Official documentation:** [Update Heartbeat Monitor](https://docs.pinghome.io/monitoring/heartbeat-monitoring/update-heartbeat-monitor/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The unique ID of the heartbeat monitor. |
| `name` | body | `string` | yes | The name of the heartbeat resource. |
| `service_id` | body | `string` | yes | The service associated with the heartbeat. |
| `interval` | body | `number` | yes | The heartbeat interval in seconds. |
| `methods[]` | body | `array<string>` | yes | The HTTP methods allowed for heartbeat check-ins. |
| `enabled` | body | `boolean` | yes | Whether the heartbeat monitor is enabled. |

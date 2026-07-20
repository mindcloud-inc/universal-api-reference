# Change Uptime Monitor Status with Pinghome

Updates uptime monitor status in Pinghome.

## Endpoint

- **Method:** `PUT`
- **Path:** `/resource-cmd/v1/resource/:id/status`
- **Base URL:** `https://api.pinghome.io`
- **Official documentation:** [Change Uptime Monitor Status](https://docs.pinghome.io/monitoring/uptime-monitoring/change-uptime-monitor-status/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The unique ID of the uptime monitor. |
| `enabled` | body | `boolean` | yes | Whether the monitor should be enabled. |

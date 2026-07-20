# Setup Heartbeat Monitor with Pinghome

Creates a new heartbeat monitor in Pinghome.

## Endpoint

- **Method:** `POST`
- **Path:** `/resource-cmd/v1/heartbeat`
- **Base URL:** `https://api.pinghome.io`
- **Official documentation:** [Setup Heartbeat Monitor](https://docs.pinghome.io/monitoring/heartbeat-monitoring/setup-heartbeat-monitor/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `service_id` | body | `string` | yes | The unique service ID associated with the heartbeat resource. |
| `name` | body | `string` | yes | — |
| `interval` | body | `number` | yes | The expected heartbeat check-in interval in seconds. |
| `enabled` | body | `boolean` | no | Whether the heartbeat monitor is enabled. |

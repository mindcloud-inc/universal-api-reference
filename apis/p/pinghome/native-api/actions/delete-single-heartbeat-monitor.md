# Delete Single Heartbeat Monitor with Pinghome

Deletes an existing heartbeat monitor from Pinghome.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/resource-cmd/v1/heartbeat/:id`
- **Base URL:** `https://api.pinghome.io`
- **Official documentation:** [Delete Single Heartbeat Monitor](https://docs.pinghome.io/monitoring/heartbeat-monitoring/delete-single-heartbeat-monitor/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The unique ID of the heartbeat monitor. |

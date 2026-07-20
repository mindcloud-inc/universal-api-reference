# Get Specific Heartbeat Information with Pinghome

Retrieves specific heartbeat information from Pinghome.

## Endpoint

- **Method:** `GET`
- **Path:** `/resource-query/v1/heartbeat/:id`
- **Base URL:** `https://api.pinghome.io`
- **Official documentation:** [Get Specific Heartbeat Information](https://docs.pinghome.io/monitoring/heartbeat-monitoring/get-specific-heartbeat-information/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The unique ID of the heartbeat monitor. |

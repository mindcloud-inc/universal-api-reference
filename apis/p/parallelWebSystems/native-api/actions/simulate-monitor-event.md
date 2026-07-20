# Simulate Monitor Event with Parallel Web Systems

## Endpoint

- **Method:** `POST`
- **Path:** `/v1alpha/monitors/:monitor_id/simulate_event`
- **Base URL:** `https://api.parallel.ai`
- **Official documentation:** [Simulate Monitor Event](https://docs.parallel.ai/api-reference/monitor/simulate-event)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `monitor_id` | path | `string` | yes | The Parallel monitor ID. |
| `event_type` | query | `string` | no | Event type to simulate. Accepted values: `0`, `1`, `2`. |

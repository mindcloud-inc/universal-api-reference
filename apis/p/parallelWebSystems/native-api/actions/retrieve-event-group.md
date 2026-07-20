# Retrieve Event Group with Parallel Web Systems

## Endpoint

- **Method:** `GET`
- **Path:** `/v1alpha/monitors/:monitor_id/event_groups/:event_group_id`
- **Base URL:** `https://api.parallel.ai`
- **Official documentation:** [Retrieve Event Group](https://docs.parallel.ai/api-reference/monitor/retrieve-event-group)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `event_group_id` | path | `string` | yes | The Parallel event group ID. |
| `monitor_id` | path | `string` | yes | The Parallel monitor ID. |

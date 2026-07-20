# Stream FindAll Events with Parallel Web Systems

## Endpoint

- **Method:** `GET`
- **Path:** `/v1beta/findall/runs/:findall_id/events`
- **Base URL:** `https://api.parallel.ai`
- **Official documentation:** [Stream FindAll Events](https://docs.parallel.ai/api-reference/findall-api-beta/stream-findall-events)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `findall_id` | path | `string` | yes | The Parallel FindAll run ID. |
| `last_event_id` | query | `string` | no | Resume streaming after this event ID. |
| `timeout` | query | `number` | no | Long-poll timeout in seconds. |

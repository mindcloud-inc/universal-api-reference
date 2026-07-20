# Stream Task Group Events with Parallel Web Systems

## Endpoint

- **Method:** `GET`
- **Path:** `/v1beta/tasks/groups/:taskgroup_id/events`
- **Base URL:** `https://api.parallel.ai`
- **Official documentation:** [Stream Task Group Events](https://docs.parallel.ai/api-reference/task-groups-beta/stream-task-group-events)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taskgroup_id` | path | `string` | yes | The Parallel task group ID. |
| `last_event_id` | query | `string` | no | Resume streaming after this event ID. |
| `timeout` | query | `number` | no | Long-poll timeout in seconds. |

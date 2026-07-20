# Fetch Task Group Runs with Parallel Web Systems

## Endpoint

- **Method:** `GET`
- **Path:** `/v1beta/tasks/groups/:taskgroup_id/runs`
- **Base URL:** `https://api.parallel.ai`
- **Official documentation:** [Fetch Task Group Runs](https://docs.parallel.ai/api-reference/task-groups-beta/fetch-task-group-runs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taskgroup_id` | path | `string` | yes | The Parallel task group ID. |
| `last_event_id` | query | `string` | no | Return runs after this event ID. |
| `status` | query | `string` | no | Filter task group runs by status. Accepted values: `0`, `1`, `2`, `3`, `4`, `5`, `6`. |
| `include_input` | query | `boolean` | no | Include task run input payloads. |
| `include_output` | query | `boolean` | no | Include task run output payloads. |

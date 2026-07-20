# Retrieve Task Group Run with Parallel Web Systems

## Endpoint

- **Method:** `GET`
- **Path:** `/v1beta/tasks/groups/:taskgroup_id/runs/:run_id`
- **Base URL:** `https://api.parallel.ai`
- **Official documentation:** [Retrieve Task Group Run](https://docs.parallel.ai/api-reference/task-groups-beta/retrieve-task-group-run)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `run_id` | path | `string` | yes | The Parallel task run ID. |
| `taskgroup_id` | path | `string` | yes | The Parallel task group ID. |

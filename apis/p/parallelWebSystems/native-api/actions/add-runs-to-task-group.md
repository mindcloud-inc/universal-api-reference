# Add Runs to Task Group with Parallel Web Systems

## Endpoint

- **Method:** `POST`
- **Path:** `/v1beta/tasks/groups/:taskgroup_id/runs`
- **Base URL:** `https://api.parallel.ai`
- **Official documentation:** [Add Runs to Task Group](https://docs.parallel.ai/api-reference/task-groups-beta/add-runs-to-task-group)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taskgroup_id` | path | `string` | yes | The Parallel task group ID. |
| `refresh_status` | query | `boolean` | no | Refresh the task group status after adding runs. |

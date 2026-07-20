# Get Goal By Key with Convert

Retrieves a goal from Convert by key.

## Endpoint

- **Method:** `GET`
- **Path:** `/accounts/:account_id/projects/:project_id/goals/:goal_key`
- **Base URL:** `https://api.convert.com/api/v2`
- **Official documentation:** [Get Goal By Key](https://api.convert.com/doc/v2/#tag/Goals/operation/getGoalByKey)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Convert project ID. |
| `goal_key` | path | `string` | yes | Convert goal key. |

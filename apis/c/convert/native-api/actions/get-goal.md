# Get Goal with Convert

Retrieves a goal from a Convert project.

## Endpoint

- **Method:** `GET`
- **Path:** `/accounts/:account_id/projects/:project_id/goals/:goal_id`
- **Base URL:** `https://api.convert.com/api/v2`
- **Official documentation:** [Get Goal](https://api.convert.com/doc/v2/#tag/Goals/operation/getGoal)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Convert project ID. |
| `goal_id` | path | `string` | yes | Convert goal ID. |

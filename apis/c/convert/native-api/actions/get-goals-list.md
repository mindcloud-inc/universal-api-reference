# List Goals with Convert

Retrieves goals from a Convert project.

## Endpoint

- **Method:** `POST`
- **Path:** `/accounts/:account_id/projects/:project_id/goals`
- **Base URL:** `https://api.convert.com/api/v2`
- **Official documentation:** [List Goals](https://api.convert.com/doc/v2/#tag/Goals/operation/getGoalsList)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Convert project ID. |

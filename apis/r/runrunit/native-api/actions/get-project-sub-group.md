# Get Project Sub Group with Runrun.it

Retrieves a project subgroup from Runrun.it.

## Endpoint

- **Method:** `GET`
- **Path:** `/project_groups/:project_group_id/project_sub_groups/:id`
- **Base URL:** `https://runrun.it/api/v1.0`
- **Official documentation:** [Get Project Sub Group](https://runrun.it/api/documentation#project-sub-groups-show-a-project-sub-group)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_group_id` | path | `string` | yes | Project Group Id path parameter. |
| `id` | path | `string` | yes | Id path parameter. |

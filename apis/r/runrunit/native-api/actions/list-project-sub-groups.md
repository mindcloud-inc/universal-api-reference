# List Project Sub Groups with Runrun.it

Retrieves project subgroups from Runrun.it.

## Endpoint

- **Method:** `GET`
- **Path:** `/project_groups/:project_group_id/project_sub_groups`
- **Base URL:** `https://runrun.it/api/v1.0`
- **Official documentation:** [List Project Sub Groups](https://runrun.it/api/documentation#project-sub-groups-list-all-project-sub-groups-using-project-group-id)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_group_id` | path | `string` | yes | Project Group Id path parameter. |

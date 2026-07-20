# List Project Flow Board Groups with Zeplin

Retrieves a list of project flow board groups from Zeplin.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/{project_id}/flow_boards/{flow_board_id}/groups`
- **Base URL:** `https://api.zeplin.dev/v1`
- **Official documentation:** [List Project Flow Board Groups](https://docs.zeplin.dev/reference/getprojectflowboardgroups)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Project id |
| `flow_board_id` | path | `string` | yes | Flow Board id |

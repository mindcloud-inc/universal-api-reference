# Get Project Flow Board with Zeplin

Retrieves a project flow board from Zeplin.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/{project_id}/flow_boards/{flow_board_id}`
- **Base URL:** `https://api.zeplin.dev/v1`
- **Official documentation:** [Get Project Flow Board](https://docs.zeplin.dev/reference/getprojectflowboard)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Project id |
| `flow_board_id` | path | `string` | yes | Flow Board id |

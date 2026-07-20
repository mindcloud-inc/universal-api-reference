# Get Project Flow Board Node with Zeplin

Retrieves a project flow board node from Zeplin.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/{project_id}/flow_boards/{flow_board_id}/nodes/{node_id}`
- **Base URL:** `https://api.zeplin.dev/v1`
- **Official documentation:** [Get Project Flow Board Node](https://docs.zeplin.dev/reference/getprojectflowboardnode)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Project id |
| `flow_board_id` | path | `string` | yes | Flow Board id |
| `node_id` | path | `string` | yes | Board node id |

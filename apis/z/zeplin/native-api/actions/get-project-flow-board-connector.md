# Get Project Flow Board Connector with Zeplin

Retrieves a project flow board connector from Zeplin.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/{project_id}/flow_boards/{flow_board_id}/connectors/{connector_id}`
- **Base URL:** `https://api.zeplin.dev/v1`
- **Official documentation:** [Get Project Flow Board Connector](https://docs.zeplin.dev/reference/getprojectflowboardconnector)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Project id |
| `flow_board_id` | path | `string` | yes | Flow Board id |
| `connector_id` | path | `string` | yes | Board connector id |

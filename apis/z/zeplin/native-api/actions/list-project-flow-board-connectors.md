# List Project Flow Board Connectors with Zeplin

Retrieves a list of project flow board connectors from Zeplin.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/{project_id}/flow_boards/{flow_board_id}/connectors`
- **Base URL:** `https://api.zeplin.dev/v1`
- **Official documentation:** [List Project Flow Board Connectors](https://docs.zeplin.dev/reference/getprojectflowboardconnectors)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Project id |
| `flow_board_id` | path | `string` | yes | Flow Board id |
| `starting_node_id` | query | `string` | no | Starting node id |
| `ending_node_id` | query | `string` | no | Ending node id |

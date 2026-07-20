# List Project Flow Board Nodes with Zeplin

Retrieves a list of project flow board nodes from Zeplin.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/{project_id}/flow_boards/{flow_board_id}/nodes`
- **Base URL:** `https://api.zeplin.dev/v1`
- **Official documentation:** [List Project Flow Board Nodes](https://docs.zeplin.dev/reference/getprojectflowboardnodes)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Project id |
| `flow_board_id` | path | `string` | yes | Flow Board id |
| `group_id` | query | `string` | no | Group id |

# Get Workflow Node Permissions with Port API AI

## Endpoint

- **Method:** `GET`
- **Path:** `/workflows/:workflow_identifier/nodes/:node_identifier/permissions`
- **Base URL:** `https://api.port.io/v1`
- **Official documentation:** [Get Workflow Node Permissions](https://docs.port.io/api-reference/get-a-workflows-node-permissions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `node_identifier` | path | `string` | yes | The workflow node identifier. |
| `workflow_identifier` | path | `string` | yes | The workflow identifier. |

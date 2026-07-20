# Update Workflow Node Permissions with Port API AI

## Endpoint

- **Method:** `PATCH`
- **Path:** `/workflows/:workflow_identifier/nodes/:node_identifier/permissions`
- **Base URL:** `https://api.port.io/v1`
- **Official documentation:** [Update Workflow Node Permissions](https://docs.port.io/api-reference/update-a-workflows-node-permissions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `node_identifier` | path | `string` | yes | The workflow node identifier. |
| `workflow_identifier` | path | `string` | yes | The workflow identifier. |
| `read` | body | `boolean` | yes | Whether the node can be viewed. |
| `update` | body | `boolean` | yes | Whether the node can be updated. |

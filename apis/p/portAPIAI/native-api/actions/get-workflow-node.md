# Get Workflow Node with Port API AI

Retrieves a workflow node from Port.

## Endpoint

- **Method:** `GET`
- **Path:** `/workflows/:workflow_identifier/nodes/:node_identifier`
- **Base URL:** `https://api.port.io/v1`
- **Official documentation:** [Get Workflow Node](https://docs.port.io/api-reference/get-a-workflows-node)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `node_identifier` | path | `string` | yes | The workflow node identifier. |
| `workflow_identifier` | path | `string` | yes | The workflow identifier. |

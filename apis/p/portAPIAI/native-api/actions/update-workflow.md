# Update Workflow with Port API AI

Updates a workflow in Port.

## Endpoint

- **Method:** `PUT`
- **Path:** `/workflows/:workflow_identifier`
- **Base URL:** `https://api.port.io/v1`
- **Official documentation:** [Update Workflow](https://docs.port.io/api-reference/change-a-workflow)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workflow_identifier` | path | `string` | yes | The Port workflow identifier. |
| `identifier` | body | `string` | yes | — |
| `nodes[]` | body | `array<object>` | yes | — |
| `title` | body | `string` | no | — |
| `icon` | body | `string` | no | — |
| `connections[]` | body | `array<object>` | no | — |

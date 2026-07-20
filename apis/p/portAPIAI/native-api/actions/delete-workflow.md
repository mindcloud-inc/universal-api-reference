# Delete Workflow with Port API AI

Deletes a workflow from Port.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/workflows/:workflow_identifier`
- **Base URL:** `https://api.port.io/v1`
- **Official documentation:** [Delete Workflow](https://docs.port.io/api-reference/delete-a-workflow)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workflow_identifier` | path | `string` | yes | The Port workflow identifier. |

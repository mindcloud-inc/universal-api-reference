# Trigger Workflow Run with Port API AI

Creates a workflow run in Port.

## Endpoint

- **Method:** `POST`
- **Path:** `/workflows/:workflow_identifier/runs`
- **Base URL:** `https://api.port.io/v1`
- **Official documentation:** [Trigger Workflow Run](https://docs.port.io/api-reference/trigger-a-workflow-run)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workflow_identifier` | path | `string` | yes | The workflow identifier. |
| `inputs` | body | `object` | yes | — |

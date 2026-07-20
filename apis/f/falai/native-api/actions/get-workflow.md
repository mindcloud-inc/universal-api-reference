# Get Workflow with fal.ai

Retrieves detailed workflow information from fal.ai.

## Endpoint

- **Method:** `GET`
- **Path:** `/workflows/:username/:workflowName`
- **Base URL:** `https://api.fal.ai/v1`
- **Official documentation:** [Get Workflow](https://fal.ai/docs/api-reference/platform-apis)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `username` | path | `string` | yes | fal.ai username that owns the workflow. |
| `workflowName` | path | `string` | yes | Workflow slug or name. |

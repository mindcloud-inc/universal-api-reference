# Create Workflow with Clarifai

Creates a new workflow in Clarifai.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/users/me/apps/:appId/workflows`
- **Base URL:** `https://api.clarifai.com`
- **Official documentation:** [Create Workflow](https://docs.clarifai.com/create/workflows/create/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appId` | path | `string` | yes | Clarifai app ID. |
| `workflows[]` | body | `array<object>` | yes | Workflows to create. |
| `workflows[].id` | body | `string` | yes | Workflow ID. |
| `workflows[].nodes[]` | body | `array<object>` | yes | Workflow nodes. |
| `workflows[].nodes[].id` | body | `string` | yes | Workflow node ID. |
| `workflows[].nodes[].model` | body | `object` | yes | Model used by the node. |
| `workflows[].nodes[].model.id` | body | `string` | yes | Model ID. |
| `workflows[].nodes[].model.user_id` | body | `string` | yes | Model owner user ID. |
| `workflows[].nodes[].model.app_id` | body | `string` | yes | Model app ID. |
| `workflows[].nodes[].model.model_version` | body | `object` | yes | Model version for the node. |
| `workflows[].nodes[].model.model_version.id` | body | `string` | yes | Model version ID. |

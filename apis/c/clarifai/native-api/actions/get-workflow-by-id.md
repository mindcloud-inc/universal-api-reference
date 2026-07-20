# Get Workflow By ID with Clarifai

Retrieves a workflow from Clarifai.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/users/me/apps/:appId/workflows/:workflowId`
- **Base URL:** `https://api.clarifai.com`
- **Official documentation:** [Get Workflow By ID](https://docs.clarifai.com/create/workflows/manage/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appId` | path | `string` | yes | Clarifai app ID. |
| `workflowId` | path | `string` | yes | Clarifai workflow ID. |

# Delete Workflow with Clarifai

Deletes an existing workflow from Clarifai.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v2/users/{userId}/apps/{{appId}}/workflows/{{workflowId}}`
- **Base URL:** `https://api.clarifai.com`
- **Official documentation:** [Delete Workflow](https://docs.clarifai.com/create/workflows/manage/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appId` | path | `string` | no | Clarifai app ID. |
| `workflowId` | path | `string` | no | Clarifai workflow ID. |

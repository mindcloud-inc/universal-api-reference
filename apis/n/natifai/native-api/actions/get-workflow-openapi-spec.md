# Get Workflow OpenAPI Spec with Natif.ai

Retrieves the OpenAPI spec for a Natif.ai workflow.

## Endpoint

- **Method:** `GET`
- **Path:** `/processing/[:workflowId]/openapi`
- **Base URL:** `https://api.natif.ai`
- **Official documentation:** [Get Workflow OpenAPI Spec](https://api.natif.ai/docs#/Document%20Capturing/get_openapi_json_processing__workflow_id__openapi_get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workflowId` | path | `string` | yes | Workflow identifier. |

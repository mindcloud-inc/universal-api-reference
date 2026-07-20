# Create Workflow with Nanonets OCR

## Endpoint

- **Method:** `POST`
- **Path:** `/workflows`
- **Base URL:** `https://app.nanonets.com/api/v4`
- **Official documentation:** [Create Workflow](https://apidocs.nanonets.com/docs/api/workflow-management/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workflow_type` | body | `string` | no | Workflow type identifier from Get Available Workflow Types. |
| `description` | body | `string` | no | Description for the new workflow. |

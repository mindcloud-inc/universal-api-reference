# Create Workflow Channel with Unstructured

Creates a workflow notification channel in Unstructured.

## Endpoint

- **Method:** `POST`
- **Path:** `/workflows/:workflow_id/notifications/channels`
- **Base URL:** `https://platform.unstructuredapp.io/api/v1`
- **Official documentation:** [Create Workflow Channel](https://docs.unstructured.io/api-reference/workflows/create-workflow-channel)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workflow_id` | path | `string` | yes | The workflow ID. |

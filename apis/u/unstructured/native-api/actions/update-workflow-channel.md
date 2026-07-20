# Update Workflow Channel with Unstructured

Updates a workflow notification channel in Unstructured.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/workflows/:workflow_id/notifications/channels/:channel_id`
- **Base URL:** `https://platform.unstructuredapp.io/api/v1`
- **Official documentation:** [Update Workflow Channel](https://docs.unstructured.io/api-reference/workflows/update-workflow-channel)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `channel_id` | path | `string` | yes | The workflow channel ID. |
| `workflow_id` | path | `string` | yes | The workflow ID. |

# Delete Workflow Channel with Unstructured

Deletes a workflow notification channel from Unstructured.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/workflows/:workflow_id/notifications/channels/:channel_id`
- **Base URL:** `https://platform.unstructuredapp.io/api/v1`
- **Official documentation:** [Delete Workflow Channel](https://docs.unstructured.io/api-reference/workflows/delete-workflow-channel)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `channel_id` | path | `string` | yes | The workflow channel ID. |
| `workflow_id` | path | `string` | yes | The workflow ID. |

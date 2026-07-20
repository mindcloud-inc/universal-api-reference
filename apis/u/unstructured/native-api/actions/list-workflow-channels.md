# List Workflow Channels with Unstructured

Retrieves workflow notification channels from Unstructured.

## Endpoint

- **Method:** `GET`
- **Path:** `/workflows/:workflow_id/notifications/channels`
- **Base URL:** `https://platform.unstructuredapp.io/api/v1`
- **Official documentation:** [List Workflow Channels](https://docs.unstructured.io/api-reference/workflows/list-workflow-channels)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workflow_id` | path | `string` | yes | The workflow ID. |

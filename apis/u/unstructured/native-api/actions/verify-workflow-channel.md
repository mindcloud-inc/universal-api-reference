# Verify Workflow Channel with Unstructured

Verifies a workflow notification channel in Unstructured.

## Endpoint

- **Method:** `POST`
- **Path:** `/workflows/:workflow_id/notifications/channels/:channel_id/verify`
- **Base URL:** `https://platform.unstructuredapp.io/api/v1`
- **Official documentation:** [Verify Workflow Channel](https://docs.unstructured.io/api-reference/workflows/verify-workflow-channel)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `channel_id` | path | `string` | yes | The workflow channel ID. |
| `workflow_id` | path | `string` | yes | The workflow ID. |

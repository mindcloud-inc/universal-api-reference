# Get Workflow Notification Channel with Unstructured

Retrieves a workflow notification channel from Unstructured.

## Endpoint

- **Method:** `GET`
- **Path:** `/workflows/:workflow_id/notifications/channels/:channel_id`
- **Base URL:** `https://platform.unstructuredapp.io/api/v1`
- **Official documentation:** [Get Workflow Notification Channel](https://docs.unstructured.io/api-reference/webhooks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workflow_id` | path | `string` | yes | Workflow ID. |
| `channel_id` | path | `string` | yes | Workflow notification channel ID. |

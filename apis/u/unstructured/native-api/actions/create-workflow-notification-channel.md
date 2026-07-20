# Create Workflow Notification Channel with Unstructured

Creates a workflow notification channel in Unstructured.

## Endpoint

- **Method:** `POST`
- **Path:** `/workflows/:workflow_id/notifications/channels`
- **Base URL:** `https://platform.unstructuredapp.io/api/v1`
- **Official documentation:** [Create Workflow Notification Channel](https://docs.unstructured.io/api-reference/webhooks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workflow_id` | path | `string` | yes | Workflow ID. |
| `channel_type` | body | `string` | yes | Notification channel type. |
| `url` | body | `string` | yes | Webhook destination URL. |
| `event_types[]` | body | `array<string>` | yes | Events sent to the channel. |
| `description` | body | `string` | no | Notification channel description. |

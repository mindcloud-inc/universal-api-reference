# Update Workflow Notification Channel with Unstructured

Updates a workflow notification channel in Unstructured.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/workflows/:workflow_id/notifications/channels/:channel_id`
- **Base URL:** `https://platform.unstructuredapp.io/api/v1`
- **Official documentation:** [Update Workflow Notification Channel](https://docs.unstructured.io/api-reference/webhooks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workflow_id` | path | `string` | yes | Workflow ID. |
| `channel_id` | path | `string` | yes | Workflow notification channel ID. |
| `url` | body | `string` | no | Webhook destination URL. |
| `event_types[]` | body | `array<string>` | no | Events sent to the channel. |
| `description` | body | `string` | no | Notification channel description. |
| `enabled` | body | `boolean` | no | Enable or disable the channel. |

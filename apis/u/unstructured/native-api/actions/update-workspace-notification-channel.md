# Update Workspace Notification Channel with Unstructured

Updates a workspace notification channel in Unstructured.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/notifications/channels/:channel_id`
- **Base URL:** `https://platform.unstructuredapp.io/api/v1`
- **Official documentation:** [Update Workspace Notification Channel](https://docs.unstructured.io/api-reference/webhooks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `channel_id` | path | `string` | yes | Workspace notification channel ID. |
| `url` | body | `string` | no | Webhook destination URL. |
| `event_types[]` | body | `array<string>` | no | Events sent to the channel. |
| `description` | body | `string` | no | Notification channel description. |
| `enabled` | body | `boolean` | no | Enable or disable the channel. |

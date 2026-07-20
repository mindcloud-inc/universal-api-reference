# Create Workspace Notification Channel with Unstructured

Creates a workspace notification channel in Unstructured.

## Endpoint

- **Method:** `POST`
- **Path:** `/notifications/channels`
- **Base URL:** `https://platform.unstructuredapp.io/api/v1`
- **Official documentation:** [Create Workspace Notification Channel](https://docs.unstructured.io/api-reference/webhooks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `channel_type` | body | `string` | yes | Notification channel type. |
| `url` | body | `string` | yes | Webhook destination URL. |
| `event_types[]` | body | `array<string>` | yes | Events sent to the channel. |
| `description` | body | `string` | no | Notification channel description. |

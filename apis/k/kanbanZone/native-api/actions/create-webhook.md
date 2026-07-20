# Create Webhook with Kanban Zone

Creates a webhook in Kanban Zone.

## Endpoint

- **Method:** `POST`
- **Path:** `/webhooks`
- **Base URL:** `https://integrations.kanbanzone.io/v1`
- **Official documentation:** [Create Webhook](https://docs.kanbanzone.io/apiReference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `board` | body | `string` | no | Board public ID |
| `url` | body | `string` | no | A valid webhook destination URL |
| `events[]` | body | `array<string>` | yes | Webhook event names to subscribe to |
| `description` | body | `string` | no | Webhook description |
| `enabled` | body | `boolean` | no | Whether the webhook is enabled |

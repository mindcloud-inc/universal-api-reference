# Update Webhook with Kanban Zone

Updates an existing webhook in Kanban Zone.

## Endpoint

- **Method:** `PUT`
- **Path:** `/webhooks/:id`
- **Base URL:** `https://integrations.kanbanzone.io/v1`
- **Official documentation:** [Update Webhook](https://docs.kanbanzone.io/apiReference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The unique ID of the webhook to update |
| `board` | body | `string` | no | Board public ID |
| `url` | body | `string` | no | A valid webhook destination URL |
| `events[]` | body | `array<string>` | no | Webhook event names to subscribe to |
| `description` | body | `string` | no | Webhook description |
| `enabled` | body | `boolean` | no | Whether the webhook is enabled |

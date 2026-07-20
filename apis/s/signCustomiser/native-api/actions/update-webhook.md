# Update Webhook with Sign Customiser

Updates an existing webhook subscription in Sign Customiser.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/v2/webhooks/:webhookId`
- **Base URL:** `https://web.signcustomiser.com`
- **Official documentation:** [Update Webhook](https://www.signcustomiser.com/help/api/put-update-a-webhook/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `webhook_id` | path | `number` | yes | The ID of the webhook. |
| `topic` | body | `list` | yes | The event topic to subscribe to. Accepted values: `form:submitted`, `order:created`, `product:created`. |
| `url` | body | `string` | yes | The URL where webhook payloads will be sent. |
| `meta` | body | `object` | no | Optional metadata to store with the webhook. |

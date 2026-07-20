# Create Webhook with Sign Customiser

Creates a new webhook subscription in Sign Customiser.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/webhooks`
- **Base URL:** `https://web.signcustomiser.com`
- **Official documentation:** [Create Webhook](https://www.signcustomiser.com/help/api/post-create-a-new-webhook/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `topic` | body | `list` | yes | The event topic to subscribe to. Accepted values: `form:submitted`, `order:created`, `product:created`. |
| `url` | body | `string` | yes | The URL where webhook payloads will be sent. |
| `meta` | body | `object` | no | Optional metadata to store with the webhook. |

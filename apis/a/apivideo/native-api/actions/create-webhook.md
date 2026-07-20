# Create Webhook with api.video

Creates a new webhook in api.video.

## Endpoint

- **Method:** `POST`
- **Path:** `/webhooks`
- **Base URL:** `https://ws.api.video`
- **Official documentation:** [Create Webhook](https://docs.api.video/reference/api/Webhooks#create-webhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `events` | body | `string` | yes | Comma-separated webhook event keys. |
| `url` | body | `string` | yes | The callback URL for the webhook. |

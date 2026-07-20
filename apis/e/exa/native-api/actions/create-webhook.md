# Create Webhook with Exa

Creates a new webhook in Exa.

## Endpoint

- **Method:** `POST`
- **Path:** `/websets/v0/webhooks`
- **Base URL:** `https://api.exa.ai`
- **Official documentation:** [Create Webhook](https://exa.ai/docs/websets/api/webhooks/create-a-webhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `events[]` | body | `array<string>` | yes | Webhook events to subscribe to. |
| `metadata` | body | `object` | no | Optional webhook metadata object. |
| `url` | body | `string` | yes | HTTPS endpoint that receives webhook deliveries. |

# Create Webhook with Renderly

Creates a webhook endpoint in Renderly.

## Endpoint

- **Method:** `POST`
- **Path:** `/webhooks`
- **Base URL:** `https://renderly.video/api/v1`
- **Official documentation:** [Create Webhook](https://renderly.video/api/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `events[]` | body | `array<string>` | no | Webhook events to subscribe to. Defaults to all supported events when omitted. |
| `url` | body | `string` | yes | Webhook endpoint URL that receives Renderly event notifications. |

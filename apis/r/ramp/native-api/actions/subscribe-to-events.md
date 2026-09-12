# Subscribe To Events with Ramp

This actions is used in conjunction with the Verify Webhook Endpoint action to register a webhook event in Ramp

## Endpoint

- **Method:** `POST`
- **Path:** `webhooks`
- **Base URL:** `https://api.ramp.com/developer/v1/`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `endpoint_url` | body | `string` | yes | This is MindCloud's Webhook URL |
| `event_types[]` | body | `array<string>` | no | The event type IDs that the webhook subscribes to. Ref: https://docs.ramp.com/developer-api/v1/webhooks#available-events |

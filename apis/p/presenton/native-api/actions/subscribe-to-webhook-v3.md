# Subscribe to Webhook V3 with Presenton

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v3/webhook/subscribe`
- **Base URL:** `https://api.presenton.ai`
- **Official documentation:** [Subscribe to Webhook V3](https://docs.presenton.ai/api-reference/v3-webhook/subscribe-to-webhook-v3)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Webhook destination URL. |
| `event` | body | `string` | yes | Event name to subscribe to. |
| `secret` | body | `string` | no | Optional signing secret. |

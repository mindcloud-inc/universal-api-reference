# Subscribe to Webhook with Presenton

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/webhook/subscribe`
- **Base URL:** `https://api.presenton.ai`
- **Official documentation:** [Subscribe to Webhook](https://docs.presenton.ai/api-reference/webhook/subscribe-to-webhook-v1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Webhook destination URL. |
| `event` | body | `string` | yes | Event name to subscribe to. |
| `secret` | body | `string` | no | Optional signing secret. |

# Subscribe to Webhook with Hyperstack Certificates

## Endpoint

- **Method:** `POST`
- **Path:** `/webhook/subscribe`
- **Base URL:** `https://api.thehyperstack.com/v1`
- **Official documentation:** [Subscribe to Webhook](https://thehyperstack.com/docs/api-guide/webhook-subscribe)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `events` | body | `object<string>` | yes | Array of event names to subscribe to. Currently supported: credential.issued. |
| `url` | body | `string` | yes | The webhook URL to receive events. |

# Create Webhook with Brevo

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/webhooks`
- **Base URL:** `https://api.brevo.com`
- **Official documentation:** [Create Webhook](https://developers.brevo.com/reference/create-webhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `events` | body | `object<string>` | yes | Webhook event types to subscribe to. |
| `type` | body | `string` | yes | Webhook type, such as transactional. |
| `url` | body | `string` | yes | HTTPS endpoint URL to receive webhook events. |

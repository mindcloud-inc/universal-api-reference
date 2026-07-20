# Update Webhook with Brevo

## Endpoint

- **Method:** `PUT`
- **Path:** `/v3/webhooks/:webhookId`
- **Base URL:** `https://api.brevo.com`
- **Official documentation:** [Update Webhook](https://developers.brevo.com/reference/update-webhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | body | `string` | no | Webhook description text. |
| `events` | body | `object<string>` | no | Webhook event types to subscribe to. |
| `type` | body | `string` | no | Webhook type, such as transactional. |
| `url` | body | `string` | no | HTTPS endpoint URL to receive webhook events. |
| `webhookId` | path | `string` | yes | Webhook ID. |

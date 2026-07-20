# Create Webhook with Wooxy

Creates a new webhook in Wooxy.

## Endpoint

- **Method:** `POST`
- **Path:** `v3/webhook/create`
- **Base URL:** `https://api.wooxy.com`
- **Official documentation:** [Create Webhook](https://wooxy.com/api-documentation/webhooks/webhook-create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | yes | Webhook title. |
| `url` | body | `string` | yes | Callback URL that receives webhook events. |
| `domainId` | body | `string` | no | Verified Wooxy domain ID. |
| `domain` | body | `string` | no | Verified Wooxy domain name. |
| `events[]` | body | `array<string>` | yes | Webhook event names. |

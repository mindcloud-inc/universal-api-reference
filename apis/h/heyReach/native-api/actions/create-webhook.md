# Create Webhook with Hey Reach

Creates a new webhook in Hey Reach.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/public/webhooks/CreateWebhook`
- **Base URL:** `https://api.heyreach.io`
- **Official documentation:** [Create Webhook](https://documenter.getpostman.com/view/23808049/2sA2xb5F75)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `webhookName` | body | `string` | yes |
| `webhookUrl` | body | `string` | yes |
| `eventType` | body | `string` | yes |
| `campaignIds[]` | body | `array<number>` | no |

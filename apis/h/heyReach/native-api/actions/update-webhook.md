# Update Webhook with Hey Reach

Updates an existing webhook in Hey Reach.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/public/webhooks/UpdateWebhook`
- **Base URL:** `https://api.heyreach.io`
- **Official documentation:** [Update Webhook](https://documenter.getpostman.com/view/23808049/2sA2xb5F75)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `webhookId` | query | `string` | yes |
| `webhookName` | body | `string` | no |
| `webhookUrl` | body | `string` | no |
| `eventType` | body | `string` | no |
| `campaignIds[]` | body | `array<number>` | no |
| `isActive` | body | `boolean` | no |

# Update Notification Webhook with Rachio Smart Hose Timer

Updates an existing notification webhook in Rachio.

## Endpoint

- **Method:** `PUT`
- **Path:** `/public/notification/webhook`
- **Base URL:** `https://api.rach.io/1`
- **Official documentation:** [Update Notification Webhook](https://rachio.readme.io/reference/publicnotificationwebhook-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `device.id` | body | `string` | yes | Device id for the webhook |
| `eventTypes[]` | body | `array<object>` | yes | Webhook event type objects |
| `externalId` | body | `string` | no | Optional external identifier |
| `id` | body | `string` | yes | Webhook id |
| `url` | body | `string` | yes | Webhook callback URL |

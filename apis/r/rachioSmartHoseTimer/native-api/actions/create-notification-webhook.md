# Create Notification Webhook with Rachio Smart Hose Timer

Creates a notification webhook for a Rachio device.

## Endpoint

- **Method:** `POST`
- **Path:** `/public/notification/webhook`
- **Base URL:** `https://api.rach.io/1`
- **Official documentation:** [Create Notification Webhook](https://rachio.readme.io/reference/publicnotificationwebhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `device.id` | body | `string` | yes | Controller device UUID for the webhook target. |
| `url` | body | `string` | yes | Webhook destination URL. |
| `externalId` | body | `string` | no | Opaque external identifier returned in webhook deliveries. |
| `eventTypes[]` | body | `array<object>` | yes | Array of notification webhook event type objects; each item should include an event type id from List Notification Webhook Event Types. |

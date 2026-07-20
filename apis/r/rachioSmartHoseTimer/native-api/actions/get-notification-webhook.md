# Get Notification Webhook with Rachio Smart Hose Timer

Retrieves a notification webhook from Rachio.

## Endpoint

- **Method:** `GET`
- **Path:** `/public/notification/webhook/:id`
- **Base URL:** `https://api.rach.io/1`
- **Official documentation:** [Get Notification Webhook](https://rachio.readme.io/reference/publicnotificationwebhookid-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Notification webhook UUID. |

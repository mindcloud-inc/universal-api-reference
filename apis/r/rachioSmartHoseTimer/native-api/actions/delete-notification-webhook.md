# Delete Notification Webhook with Rachio Smart Hose Timer

Deletes an existing notification webhook from Rachio.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/public/notification/webhook/:id`
- **Base URL:** `https://api.rach.io/1`
- **Official documentation:** [Delete Notification Webhook](https://rachio.readme.io/reference/publicnotificationwebhookid)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Webhook Id to remove |

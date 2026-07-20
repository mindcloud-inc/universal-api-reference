# Update Webhook with Rachio Smart Hose Timer

Updates an existing webhook in Rachio.

## Endpoint

- **Method:** `PUT`
- **Path:** `https://cloud-rest.rach.io/webhook/updateWebhook`
- **Base URL:** `https://api.rach.io/1`
- **Official documentation:** [Update Webhook](https://rachio.readme.io/reference/webhookservice_updatewebhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `event_types` | body | `object` | no | event_types object for updating subscribed event types. |
| `external_id` | body | `object` | no | external_id object. Set data to the new value, or null to remove it. |
| `id` | body | `string` | yes | Webhook id |
| `resource_id` | body | `object` | no | resource_id object for the target webhook resource. |
| `url` | body | `string` | no | Webhook callback URL |

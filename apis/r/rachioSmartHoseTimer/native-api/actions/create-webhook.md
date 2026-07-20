# Create Webhook with Rachio Smart Hose Timer

Creates a new webhook in Rachio.

## Endpoint

- **Method:** `POST`
- **Path:** `https://cloud-rest.rach.io/webhook/createWebhook`
- **Base URL:** `https://api.rach.io/1`
- **Official documentation:** [Create Webhook](https://rachio.readme.io/reference/webhookservice_createwebhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `resource_id` | body | `object` | yes | Webhook target resource object, for example {"valveId":"uuid"} or {"irrigationControllerId":"uuid"}. |
| `url` | body | `string` | yes | Webhook destination URL. |
| `external_id` | body | `string` | no | Opaque identifier echoed back in webhook deliveries. |
| `event_types[]` | body | `array<string>` | yes | Array of webhook event type strings from List Webhook Event Types. |

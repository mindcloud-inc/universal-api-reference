# Get Webhook with Rachio Smart Hose Timer

Retrieves a configured webhook from Rachio.

## Endpoint

- **Method:** `GET`
- **Path:** `https://cloud-rest.rach.io/webhook/getWebhook/:id`
- **Base URL:** `https://api.rach.io/1`
- **Official documentation:** [Get Webhook](https://rachio.readme.io/reference/webhookservice_getwebhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Webhook UUID. |

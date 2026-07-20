# List Webhooks with Rachio Smart Hose Timer

Retrieves configured webhooks from your Rachio account.

## Endpoint

- **Method:** `GET`
- **Path:** `https://cloud-rest.rach.io/webhook/listWebhooks`
- **Base URL:** `https://api.rach.io/1`
- **Official documentation:** [List Webhooks](https://rachio.readme.io/reference/webhookservice_listwebhooks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `resource_id.irrigation_controller_id` | query | `string` | no | Filter by irrigation controller UUID. |
| `resource_id.lighting_controller_id` | query | `string` | no | Filter by lighting controller UUID. |
| `resource_id.program_id` | query | `string` | no | Filter by program UUID. |
| `resource_id.valve_id` | query | `string` | no | Filter by valve UUID. |

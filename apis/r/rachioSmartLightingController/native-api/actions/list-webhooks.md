# List Webhooks with Rachio Smart Lighting Controller

## Endpoint

- **Method:** `GET`
- **Path:** `https://cloud-rest.rach.io/webhook/listWebhooks`
- **Base URL:** `https://cloud-rest.rach.io`
- **Official documentation:** [List Webhooks](https://rachio.readme.io/reference/webhookservice_listwebhooks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `resource_id.irrigation_controller_id` | query | `string` | no | Limit results to an irrigation controller. |
| `resource_id.lighting_controller_id` | query | `string` | no | Limit results to a lighting controller. |
| `resource_id.program_id` | query | `string` | no | Limit results to a program. |
| `resource_id.valve_id` | query | `string` | no | Limit results to a valve. |

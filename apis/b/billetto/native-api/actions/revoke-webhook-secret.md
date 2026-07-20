# Revoke Webhook Secret with Billetto

Deletes a webhook secret from Billetto.

## Endpoint

- **Method:** `DELETE`
- **Path:** `organiser/webhooks/{webhook_id}/secrets/{id}`
- **Base URL:** `https://billetto.dk/api/v3`
- **Official documentation:** [Revoke Webhook Secret](https://api.billetto.com/reference/revoke-a-webhook-secret-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `webhook_id` | path | `string` | yes | Billetto webhook ID. |
| `id` | path | `string` | yes | Billetto webhook secret ID. |

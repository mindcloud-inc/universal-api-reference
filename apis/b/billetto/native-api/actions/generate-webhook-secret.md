# Generate Webhook Secret with Billetto

Creates a webhook secret in Billetto.

## Endpoint

- **Method:** `POST`
- **Path:** `organiser/webhooks/{id}/secrets`
- **Base URL:** `https://billetto.dk/api/v3`
- **Official documentation:** [Generate Webhook Secret](https://api.billetto.com/reference/generate-a-webhook-secret-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Billetto webhook ID. |

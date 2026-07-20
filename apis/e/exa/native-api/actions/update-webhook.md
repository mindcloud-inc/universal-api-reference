# Update Webhook with Exa

Updates an existing webhook in Exa.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/websets/v0/webhooks/:id`
- **Base URL:** `https://api.exa.ai`
- **Official documentation:** [Update Webhook](https://exa.ai/docs/websets/api/webhooks/update-a-webhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `events[]` | body | `array<string>` | no | Updated webhook events. |
| `id` | path | `string` | yes | Webhook identifier. |
| `metadata` | body | `object` | no | Updated webhook metadata object. |
| `url` | body | `string` | no | Updated HTTPS endpoint URL. |

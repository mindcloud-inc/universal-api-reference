# Add Webhook with Explorium

Creates a webhook in Explorium API.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/webhooks`
- **Base URL:** `https://api.explorium.ai`
- **Official documentation:** [Add Webhook](https://developers.explorium.ai/reference/webhooks/add_webhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `partner_id` | body | `string` | yes | The partner identifier used for the webhook. |
| `webhook_url` | body | `string` | yes | The URL that should receive webhook callbacks. |

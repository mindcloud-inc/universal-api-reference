# Create Webhook with Lightspeed Retail POS (X-Series)

Creates a new webhook in Lightspeed Retail POS (X-Series).

## Endpoint

- **Method:** `POST`
- **Path:** `/api/2.0/webhooks`
- **Base URL:** `https://{domain_prefix}.retail.lightspeed.app`
- **Official documentation:** [Create Webhook](https://x-series-api.lightspeedhq.com/reference/post-webhooks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | The destination URL for webhook deliveries. |
| `type` | body | `string` | yes | The webhook event type. |
| `active` | body | `boolean` | yes | Whether the webhook is active. |

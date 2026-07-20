# Update Webhook with Lightspeed Retail POS (X-Series)

Updates an existing webhook in Lightspeed Retail POS (X-Series).

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/2.0/webhooks/:webhookId`
- **Base URL:** `https://{domain_prefix}.retail.lightspeed.app`
- **Official documentation:** [Update Webhook](https://x-series-api.lightspeedhq.com/reference/put-webhooks-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `webhookId` | path | `string` | yes | The webhook ID to update |
| `url` | body | `string` | yes | Updated webhook URL |
| `type` | body | `string` | yes | Webhook event type |
| `active` | body | `boolean` | yes | Whether the webhook is active |

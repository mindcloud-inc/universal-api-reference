# Create Webhook Subscription with Alegra

Creates a webhook subscription in Alegra.

## Endpoint

- **Method:** `POST`
- **Path:** `/webhooks/subscriptions`
- **Base URL:** `https://api.alegra.com/api/v1`
- **Official documentation:** [Create Webhook Subscription](https://developer.alegra.com/reference/post_webhooks-subscriptions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `event` | body | `string` | yes | Accepted values: `0`, `1`, `10`, `11`, `2`, `3`, `4`, `5`, `6`, `7`, `8`, `9`. |
| `url` | body | `string` | yes | — |

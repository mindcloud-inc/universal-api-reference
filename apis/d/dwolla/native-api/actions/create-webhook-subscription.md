# Create Webhook Subscription with Dwolla

Creates a webhook subscription in Dwolla.

## Endpoint

- **Method:** `POST`
- **Path:** `/webhook-subscriptions`
- **Base URL:** `https://api-sandbox.dwolla.com`
- **Official documentation:** [Create Webhook Subscription](https://developers.dwolla.com/docs/api-reference/webhook-subscriptions/create-a-webhook-subscription)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Webhook delivery URL |
| `secret` | body | `string` | yes | Webhook signing secret |

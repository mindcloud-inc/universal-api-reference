# List Webhook Subscriptions with Userflow

Retrieves a list of webhook subscriptions from Userflow.

## Endpoint

- **Method:** `GET`
- **Path:** `/webhook_subscriptions`
- **Base URL:** `https://api.userflow.com`
- **Official documentation:** [List Webhook Subscriptions](https://docs.userflow.com/docs/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | Maximum number of webhook subscriptions to return. |
| `order_by` | query | `string` | no | Sort webhook subscriptions by created_at or url. |
| `starting_after` | query | `string` | no | Return webhook subscriptions after this subscription ID. |

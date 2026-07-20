# Create Webhook Subscription with Paycove

Creates a webhook subscription in Paycove.

## Endpoint

- **Method:** `POST`
- **Path:** `hooks`
- **Base URL:** `https://paycove.io/api/v1`
- **Official documentation:** [Create Webhook Subscription](https://docs.paycove.io/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `target_url` | body | `string` | yes | Destination to deliver deal payload to. |
| `event` | body | `string` | yes | Webhook event type to subscribe to. |

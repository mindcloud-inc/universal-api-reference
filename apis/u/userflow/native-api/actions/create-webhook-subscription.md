# Create Webhook Subscription with Userflow

Creates a webhook subscription in Userflow.

## Endpoint

- **Method:** `POST`
- **Path:** `/webhook_subscriptions`
- **Base URL:** `https://api.userflow.com`
- **Official documentation:** [Create Webhook Subscription](https://docs.userflow.com/docs/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `api_version` | body | `string` | no | API version to use for webhook payloads. |
| `topics[]` | body | `array<string>` | yes | Webhook topics to subscribe to. |
| `url` | body | `string` | yes | Webhook destination URL. |

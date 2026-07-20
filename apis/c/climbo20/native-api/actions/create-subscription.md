# Create Subscription with Climbo 2.0

Creates a webhook subscription in Climbo 2.0.

## Endpoint

- **Method:** `POST`
- **Path:** `/webhook/subscribe`
- **Base URL:** `https://api.climbo.com`
- **Official documentation:** [Create Subscription](https://climbo.readme.io/reference/create-subscription)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Webhook target URL. |
| `events` | body | `list<string>` | yes | Webhook events to subscribe to. |

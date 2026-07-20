# Create Webhook Subscription with ProProfs Project

Creates a webhook subscription in ProProfs Project.

## Endpoint

- **Method:** `POST`
- **Path:** `/hooks`
- **Base URL:** `https://api.projectbubble.com/v2`
- **Official documentation:** [Create Webhook Subscription](https://help.proprofsproject.com/webhooks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `event` | body | `string` | yes | The webhook event to subscribe to. |
| `target_url` | body | `string` | yes | The unique URL that should receive webhook notifications. |

# Create Webhook Subscription with Scoreboard Buzz

Creates a webhook subscription in Scoreboard Buzz.

## Endpoint

- **Method:** `POST`
- **Path:** `/webhooks/subscribe`
- **Base URL:** `https://api.scoreboardbuzz.com/api/v1`
- **Official documentation:** [Create Webhook Subscription](https://docs.scoreboardbuzz.com/#/Webhooks/createWebhookSubscription)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `target_url` | body | `string` | yes | HTTPS URL that should receive webhook payloads. |

# Remove Webhook Subscription with Scoreboard Buzz

Deletes a webhook subscription from Scoreboard Buzz.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/webhooks/unsubscribe`
- **Base URL:** `https://api.scoreboardbuzz.com/api/v1`
- **Official documentation:** [Remove Webhook Subscription](https://docs.scoreboardbuzz.com/#/Webhooks/deleteWebhookSubscription)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `target_url` | body | `string` | yes | HTTPS URL of the subscription to remove. |

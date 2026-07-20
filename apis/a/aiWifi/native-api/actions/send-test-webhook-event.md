# Send test webhook event with AiWifi

Sends a test event to a webhook in AiWifi.

## Endpoint

- **Method:** `POST`
- **Path:** `/brands/{{brandId}}/webhook-configs/{{webhookId}}/event/test`
- **Base URL:** `https://api.aiwifi.io/api/v1`
- **Official documentation:** [Send test webhook event](https://help.aiwifi.io/en/category/webhook/article/logs-validation-and-testing-of-webhooks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `webhookId` | path | `number` | yes | — |
| `event` | body | `list<string>` | yes | Accepted values: `guest.connected`, `guest.data`, `guest.interests`, `surveyAnswer.created`. |

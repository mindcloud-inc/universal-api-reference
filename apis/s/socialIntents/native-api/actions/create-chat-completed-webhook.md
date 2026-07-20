# Create Chat Completed Webhook with Social Intents

Creates a chat completed webhook in Social Intents.

## Endpoint

- **Method:** `POST`
- **Path:** `/apps/:appId/webhook`
- **Base URL:** `https://www.socialintents.com/v1/api`
- **Official documentation:** [Create Chat Completed Webhook](https://www.socialintents.com/docs/integrations/webhooks-leads-transcripts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appId` | path | `string` | yes | The Social Intents widget ID that will own the webhook. |
| `target_url` | body | `string` | yes | The HTTPS endpoint Social Intents should POST webhook events to. |

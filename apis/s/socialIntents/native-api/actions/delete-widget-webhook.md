# Delete Widget Webhook with Social Intents

Deletes a widget webhook from Social Intents.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/apps/:appId/webhook/:webhookId`
- **Base URL:** `https://www.socialintents.com/v1/api`
- **Official documentation:** [Delete Widget Webhook](https://www.socialintents.com/docs/integrations/webhooks-leads-transcripts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appId` | path | `string` | yes | The Social Intents widget ID that owns the webhook. |
| `webhookId` | path | `string` | yes | The Social Intents webhook ID to delete. |

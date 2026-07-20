# Create Webhook Subscription with CheckFlow

## Endpoint

- **Method:** `POST`
- **Path:** `/api/web-hook/subscribe`
- **Base URL:** `https://app.checkflow.io`
- **Official documentation:** [Create Webhook Subscription](https://docs.checkflow.io/docs/api/webhooks#create-webhook-subscription)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `source` | query | `string` | yes | A label identifying the source of this subscription, such as custom or zapier. |
| `eventType` | query | `string` | yes | The event that triggers the webhook. |
| `targetUrl` | query | `string` | yes | The URL that CheckFlow will POST event data to. |
| `templateKey` | query | `string` | no | Required when eventType is new_checklist. |
| `taskKey` | query | `string` | no | Required when eventType is task_completed. |
| `taskContentKey` | query | `string` | no | Required when eventType is file_uploaded. |

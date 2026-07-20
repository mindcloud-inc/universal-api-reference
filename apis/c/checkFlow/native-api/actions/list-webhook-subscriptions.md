# List Webhook Subscriptions with CheckFlow

## Endpoint

- **Method:** `GET`
- **Path:** `/api/web-hook/subscriptions`
- **Base URL:** `https://app.checkflow.io`
- **Official documentation:** [List Webhook Subscriptions](https://docs.checkflow.io/docs/api/webhooks#list-webhook-subscriptions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `source` | query | `string` | no | Filters by the source of the webhook. Defaults to ALL. |
| `eventType` | query | `string` | no | Filters by event type. Defaults to ALL. |

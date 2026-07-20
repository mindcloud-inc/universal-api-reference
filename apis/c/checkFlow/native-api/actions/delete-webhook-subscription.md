# Delete Webhook Subscription with CheckFlow

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/web-hook/unsubscribe`
- **Base URL:** `https://app.checkflow.io`
- **Official documentation:** [Delete Webhook Subscription](https://docs.checkflow.io/docs/api/webhooks#delete-webhook-subscription)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `subscriptionId` | query | `string` | yes | The id of the web hook subscription you want to delete. |

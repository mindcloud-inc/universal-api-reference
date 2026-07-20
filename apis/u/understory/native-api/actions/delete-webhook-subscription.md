# Delete Webhook Subscription with Understory

Deletes an existing webhook subscription from Understory.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v1/webhook-subscriptions/{{subscriptionId}}`
- **Base URL:** `https://api.understory.io`
- **Official documentation:** [Delete Webhook Subscription](https://developer.understory.io/apis/webhook/deletewebhooksubscription.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `subscriptionId` | path | `string` | yes | The unique identifier of the subscription. |

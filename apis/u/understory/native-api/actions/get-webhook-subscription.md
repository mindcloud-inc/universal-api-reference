# Get Webhook Subscription with Understory

Retrieves a webhook subscription from Understory.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/webhook-subscriptions/{{subscriptionId}}`
- **Base URL:** `https://api.understory.io`
- **Official documentation:** [Get Webhook Subscription](https://developer.understory.io/apis/webhook/getwebhooksubscription.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `subscriptionId` | path | `string` | yes | The unique identifier of the subscription. |

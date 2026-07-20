# Update Webhook Subscription with Understory

Updates an existing webhook subscription in Understory.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/webhook-subscriptions/{{subscriptionId}}`
- **Base URL:** `https://api.understory.io`
- **Official documentation:** [Update Webhook Subscription](https://developer.understory.io/apis/webhook/updatewebhooksubscription.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `subscriptionId` | path | `string` | yes | The unique identifier of the subscription. |
| `url` | body | `string` | yes | The URL to send webhook events to. |
| `event_types[]` | body | `array<string>` | yes | One or more event types to subscribe to. |
| `state` | body | `list` | yes | The state of the subscription. Accepted values: `0`, `1`. |
| `metadata` | body | `object` | no | Optional custom metadata object for the subscription. |

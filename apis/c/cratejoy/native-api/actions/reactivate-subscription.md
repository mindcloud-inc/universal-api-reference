# Reactivate Subscription with Cratejoy

Reactivates a subscription in Cratejoy.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/subscriptions/:subscriptionId/reactivate/`
- **Base URL:** `https://api.cratejoy.com`
- **Official documentation:** [Reactivate Subscription](https://docs.cratejoy.com/reference/subscription-methods)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `subscriptionId` | path | `number` | yes | The Cratejoy subscription ID. |
| `log_note` | body | `string` | no | A note recorded when reactivating the subscription. |

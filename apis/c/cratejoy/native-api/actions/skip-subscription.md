# Skip Subscription with Cratejoy

Skips a subscription's next renewal in Cratejoy.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/subscriptions/:subscriptionId/skip/`
- **Base URL:** `https://api.cratejoy.com`
- **Official documentation:** [Skip Subscription](https://docs.cratejoy.com/reference/subscription-methods)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `subscriptionId` | path | `number` | yes | The Cratejoy subscription ID. |
| `log_note` | body | `string` | no | A note recorded when skipping the subscription. |

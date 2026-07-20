# Update Subscription with Cratejoy

Updates an existing subscription in Cratejoy.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/subscriptions/:subscriptionId/`
- **Base URL:** `https://api.cratejoy.com`
- **Official documentation:** [Update Subscription](https://docs.cratejoy.com/reference/subscription-methods)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `subscriptionId` | path | `number` | yes | The Cratejoy subscription ID. |
| `note` | body | `string` | no | A note for the subscription. |

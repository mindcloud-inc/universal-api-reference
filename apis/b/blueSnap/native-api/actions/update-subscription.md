# Update Subscription with BlueSnap

Updates a subscription in BlueSnap.

## Endpoint

- **Method:** `PUT`
- **Path:** `/recurring/subscriptions/:subscriptionId`
- **Base URL:** `https://sandbox.bluesnap.com/services/2`
- **Official documentation:** [Update Subscription](https://developers.bluesnap.com/v8976-JSON/reference/update-subscription)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `subscriptionId` | path | `string` | yes | Subscription ID. |
| `status` | body | `string` | no | Subscription status, e.g. ACTIVE or CANCELED. |

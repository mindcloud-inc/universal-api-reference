# Create Subscription with BlueSnap

Creates a subscription in BlueSnap.

## Endpoint

- **Method:** `POST`
- **Path:** `/recurring/subscriptions`
- **Base URL:** `https://sandbox.bluesnap.com/services/2`
- **Official documentation:** [Create Subscription](https://developers.bluesnap.com/v8976-JSON/reference/create-subscription)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `planId` | body | `string` | yes | Billing plan ID for the subscription. |
| `vaultedShopperId` | body | `string` | yes | Vaulted shopper ID to attach to the subscription. |

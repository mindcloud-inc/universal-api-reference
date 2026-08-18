# Retrieve Payment Method – Southern Botanical with Stripe

## Endpoint

- **Method:** `GET`
- **Path:** `payment_methods/:paymentMethodId`
- **Base URL:** `https://api.stripe.com/v1`
- **Official documentation:** [Retrieve Payment Method – Southern Botanical](https://docs.stripe.com/api/payment_methods/retrieve)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `paymentMethodId` | path | `string` | yes | Stripe PaymentMethod ID to retrieve (for example, pm_...). |

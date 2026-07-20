# Create Subscription with SureCart

## Endpoint

- **Method:** `POST`
- **Path:** `v1/subscriptions`
- **Base URL:** `https://api.surecart.com`
- **Official documentation:** [Create Subscription](https://developer.surecart.com/api-reference/subscriptions/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `subscription.customer` | body | `string` | yes | The customer ID to subscribe. |
| `subscription.price` | body | `string` | yes | The recurring price ID for the subscription. |
| `subscription.payment_method` | body | `string` | no | Optional payment method ID for paid subscriptions. |

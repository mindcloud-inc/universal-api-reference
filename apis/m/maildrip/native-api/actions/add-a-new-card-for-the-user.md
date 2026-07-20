# Add a new card for the user with Maildrip

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/payment/stripe/customer/cards`
- **Base URL:** `https://api.maildrip.io`
- **Official documentation:** [Add a new card for the user](https://api.maildrip.io/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `paymentMethodId` | body | `string` | no | The payment method ID from Stripe |

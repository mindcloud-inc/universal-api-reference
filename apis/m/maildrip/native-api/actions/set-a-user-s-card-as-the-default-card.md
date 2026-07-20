# Set a user's card as the default card with Maildrip

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v1/payment/stripe/customer/cards`
- **Base URL:** `https://api.maildrip.io`
- **Official documentation:** [Set a user's card as the default card](https://api.maildrip.io/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `paymentMethodId` | body | `string` | no | The payment method ID to set as default |

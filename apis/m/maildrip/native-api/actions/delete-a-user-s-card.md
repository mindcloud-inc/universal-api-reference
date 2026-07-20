# Delete a user's card with Maildrip

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/v1/payment/stripe/customer/cards/{id}`
- **Base URL:** `https://api.maildrip.io`
- **Official documentation:** [Delete a user's card](https://api.maildrip.io/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The payment method ID of the card to delete |

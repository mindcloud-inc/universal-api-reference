# Create Commerce User Payment Method with Goody

Creates a commerce user payment method in Goody.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/commerce_user_payment_methods`
- **Base URL:** `https://api.ongoody.com`
- **Official documentation:** [Create Commerce User Payment Method](https://developer.ongoody.com/api-reference/commerce-user-payment-methods/create-a-commerce-user-payment-method)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cardholder_name` | body | `string` | yes | The name on the card. |
| `commerce_end_user_id` | body | `string` | yes | The user ID in your app to associate this payment method with. |
| `interim_card_key` | body | `string` | yes | The temporary card token returned by Goody’s embedded payment form. |
| `billing_address` | body | `object` | yes | Billing address object. Goody’s example includes `address_1`, `address_2`, `city`, `state`, `postal_code`, and `country`. |

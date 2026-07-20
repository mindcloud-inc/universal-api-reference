# Select Payment Method with Escrow.com

Selects a transaction payment method in Escrow.com.

## Endpoint

- **Method:** `POST`
- **Path:** `/transaction/:transaction_id/payment_methods/:payment_method_name`
- **Base URL:** `https://api.escrow-sandbox.com/2017-09-01`
- **Official documentation:** [Select Payment Method](https://www.escrow.com/api/docs/reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `transaction_id` | path | `number` | yes | The Escrow.com transaction ID. |
| `payment_method_name` | path | `string` | yes | Payment method name. Documented values include credit_card, paypal, wire_transfer, and poli. Accepted values: `0`, `1`, `2`, `3`. |
| `wire_reference` | body | `string` | no | Wire reference number when selecting wire transfer. |
| `return_url` | body | `string` | no | Return URL used by PayPal or credit card payment flows. |
| `as_customer` | query | `string` | no | Escrow.com customer email to send as the As-Customer header when acting as a partner on behalf of a party. |

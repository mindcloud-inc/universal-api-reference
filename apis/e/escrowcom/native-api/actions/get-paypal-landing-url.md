# Get PayPal Landing URL with Escrow.com

Retrieves a PayPal landing URL from Escrow.com.

## Endpoint

- **Method:** `GET`
- **Path:** `/transaction/:transaction_id/payment_methods/paypal`
- **Base URL:** `https://api.escrow-sandbox.com/2017-09-01`
- **Official documentation:** [Get PayPal Landing URL](https://www.escrow.com/api/docs/reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `transaction_id` | path | `number` | yes | The Escrow.com transaction ID. |
| `return_url` | query | `string` | no | Redirect URL used after the customer is redirected to the Escrow PayPal success page. |
| `redirect_type` | query | `string` | no | Whether the redirect happens automatically or manually via CTA click. |
| `as_customer` | query | `string` | no | Escrow.com customer email to send as the As-Customer header when acting as a partner on behalf of a party. |

# Update Customer with Stripe

Updates an existing customer in Stripe.

## Endpoint

- **Method:** `POST`
- **Path:** `customers/:customer`
- **Base URL:** `https://api.stripe.com/v1`
- **Official documentation:** [Update Customer](https://docs.stripe.com/api/customers/update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customer` | path | `string` | yes | The ID of the customer to update. |
| `name` | body | `string` | no | — |
| `email` | body | `string` | no | — |
| `phone` | body | `string` | no | — |
| `description` | body | `string` | no | — |
| `metadata` | body | `object` | no | — |
| `default_source` | body | `string` | no | — |
| `source` | body | `string` | no | — |
| `address` | body | `object` | no | — |
| `shipping` | body | `object` | no | — |
| `tax_exempt` | body | `list<string>` | no | Accepted values: `exempt`, `none`, `reverse`. |
| `balance` | body | `number` | no | — |
| `cash_balance` | body | `object` | no | — |
| `invoice_prefix` | body | `string` | no | — |
| `invoice_settings` | body | `object` | no | — |
| `next_invoice_sequence` | body | `number` | no | — |
| `preferred_locales[]` | body | `array<string>` | no | — |
| `tax` | body | `object` | no | — |
| `default_bank_account` | body | `string` | no | — |
| `default_card` | body | `string` | no | — |
| `default_alipay_account` | body | `string` | no | — |
| `expand[]` | body | `array<string>` | no | — |

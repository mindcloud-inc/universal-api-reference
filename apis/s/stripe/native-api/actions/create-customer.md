# Create Customer with Stripe

Creates a new customer in Stripe.

## Endpoint

- **Method:** `POST`
- **Path:** `customers`
- **Base URL:** `https://api.stripe.com/v1`
- **Official documentation:** [Create Customer](https://docs.stripe.com/api/customers/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | no | — |
| `email` | body | `string` | no | — |
| `phone` | body | `string` | no | — |
| `description` | body | `string` | no | — |
| `metadata` | body | `object` | no | — |
| `payment_method` | body | `string` | no | — |
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
| `tax_id_data[]` | body | `array<object>` | no | — |
| `test_clock` | body | `string` | no | — |
| `expand[]` | body | `array<string>` | no | — |

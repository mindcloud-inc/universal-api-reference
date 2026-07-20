# Create Charge with Reepay

Creates a new charge in Reepay.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/charge`
- **Base URL:** `https://api.frisbii.com`
- **Official documentation:** [Create Charge](https://docs.frisbii.com/reference/createcharge)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `account_funding` | body | `boolean` | no |
| `account_funding_information` | body | `object` | no |
| `acquirer_reference` | body | `string` | no |
| `amount` | body | `number` | no |
| `async` | body | `boolean` | no |
| `billing_address` | body | `object` | no |
| `currency` | body | `string` | no |
| `customer` | body | `object` | no |
| `customer_handle` | body | `string` | no |
| `handle` | body | `string` | yes |
| `key` | body | `string` | no |
| `metadata` | body | `object` | no |
| `order_lines[]` | body | `array<object>` | no |
| `ordertext` | body | `string` | no |
| `parameters` | body | `object` | no |
| `payment_method_reference` | body | `string` | no |
| `recurring` | body | `boolean` | no |
| `settle` | body | `boolean` | no |
| `shipping_address` | body | `object` | no |
| `source` | body | `string` | yes |
| `text_on_statement` | body | `string` | no |
| `use_pm_for_subscription` | body | `boolean` | no |

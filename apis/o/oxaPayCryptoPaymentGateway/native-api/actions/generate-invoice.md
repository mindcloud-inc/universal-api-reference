# Generate Invoice with OxaPay Crypto Payment Gateway

Creates a new invoice in OxaPay.

## Endpoint

- **Method:** `POST`
- **Path:** `/payment/invoice`
- **Base URL:** `https://api.oxapay.com/v1`
- **Official documentation:** [Generate Invoice](https://docs.oxapay.com/api-reference/payment/generate-invoice)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `amount` | body | `number` | yes | Invoice amount. |
| `currency` | body | `string` | yes | Fiat currency symbol. |
| `sandbox` | body | `boolean` | no | Create a sandbox invoice. |
| `order_id` | body | `string` | no | Merchant order id. |
| `description` | body | `string` | no | Invoice description. |
| `pay_currency` | body | `string` | no | Requested crypto payment currency. |

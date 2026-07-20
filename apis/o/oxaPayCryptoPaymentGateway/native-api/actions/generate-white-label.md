# Generate White Label with OxaPay Crypto Payment Gateway

Creates a new white-label payment in OxaPay.

## Endpoint

- **Method:** `POST`
- **Path:** `/payment/white-label`
- **Base URL:** `https://api.oxapay.com/v1`
- **Official documentation:** [Generate White Label](https://docs.oxapay.com/api-reference/payment/generate-white-label2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `amount` | body | `number` | yes | White label invoice amount. |
| `pay_currency` | body | `string` | yes | Requested crypto payment currency. |
| `network` | body | `string` | yes | Blockchain network key. |
| `sandbox` | body | `boolean` | no | Create a sandbox white label payment. |
| `order_id` | body | `string` | no | Merchant order id. |

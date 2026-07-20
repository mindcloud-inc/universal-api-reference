# Generate Static Address with OxaPay Crypto Payment Gateway

Creates a new static address in OxaPay.

## Endpoint

- **Method:** `POST`
- **Path:** `/payment/static-address`
- **Base URL:** `https://api.oxapay.com/v1`
- **Official documentation:** [Generate Static Address](https://docs.oxapay.com/api-reference/payment/generate-static-address)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `to_currency` | body | `string` | no | Optional payout token or currency on the selected network. |
| `network` | body | `string` | yes | Blockchain network key. |
| `callback_url` | body | `string` | no | Webhook callback URL. |
| `email` | body | `string` | no | Customer email. |
| `order_id` | body | `string` | no | Merchant order id. |
| `description` | body | `string` | no | Static address description. |
| `sandbox` | body | `boolean` | no | Create a sandbox static address. |

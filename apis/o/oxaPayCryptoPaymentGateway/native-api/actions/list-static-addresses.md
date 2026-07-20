# List Static Addresses with OxaPay Crypto Payment Gateway

Retrieves static addresses from OxaPay.

## Endpoint

- **Method:** `GET`
- **Path:** `/payment/static-address`
- **Base URL:** `https://api.oxapay.com/v1`
- **Official documentation:** [List Static Addresses](https://docs.oxapay.com/api-reference/payment/static-address-list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `number` | no | Page number. |
| `size` | query | `number` | no | Page size. |
| `track_id` | query | `string` | no | Filter by static address track id. |
| `order_id` | query | `string` | no | Filter by merchant order id. |
| `email` | query | `string` | no | Filter by customer email. |
| `have_tx` | query | `boolean` | no | Filter static addresses with transactions. |
| `currency` | query | `string` | no | Filter by currency symbol. |
| `network` | query | `string` | no | Filter by blockchain network. |
| `address` | query | `string` | no | Filter by static address. |

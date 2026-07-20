# List Payments with OxaPay Crypto Payment Gateway

Retrieves payments from OxaPay.

## Endpoint

- **Method:** `GET`
- **Path:** `/payment`
- **Base URL:** `https://api.oxapay.com/v1`
- **Official documentation:** [List Payments](https://docs.oxapay.com/api-reference/payment/payment-history)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `number` | no | Page number. |
| `size` | query | `number` | no | Page size. |
| `track_id` | query | `string` | no | Filter by payment track id. |
| `type` | query | `string` | no | Filter by payment type. |
| `status` | query | `string` | no | Filter by payment status. |
| `pay_currency` | query | `string` | no | Filter by pay currency symbol. |
| `currency` | query | `string` | no | Filter by invoice currency symbol. |
| `network` | query | `string` | no | Filter by blockchain network. |
| `address` | query | `string` | no | Filter by destination address. |
| `from_date` | query | `number` | no | UNIX start timestamp. |
| `to_date` | query | `number` | no | UNIX end timestamp. |
| `from_amount` | query | `number` | no | Minimum amount filter. |
| `to_amount` | query | `number` | no | Maximum amount filter. |
| `sort_by` | query | `string` | no | Sort field. |
| `sort_type` | query | `string` | no | Sort direction. |

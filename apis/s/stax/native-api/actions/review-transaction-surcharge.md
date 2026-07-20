# Review Transaction Surcharge with Stax

Calculates surcharge details for a transaction in Stax.

## Endpoint

- **Method:** `GET`
- **Path:** `/surcharge/review`
- **Base URL:** `https://apiprod.fattlabs.com`
- **Official documentation:** [Review Transaction Surcharge](https://docs.staxpayments.com/reference/review-a-transactions-surcharge-information)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `payment_method_id` | query | `string` | no | Payment method identifier |
| `total` | query | `string` | no | Transaction total for surcharge review |

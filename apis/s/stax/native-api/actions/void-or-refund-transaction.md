# Void or Refund Transaction with Stax

Voids or refunds a transaction in Stax.

## Endpoint

- **Method:** `POST`
- **Path:** `/transaction/:id/void-or-refund`
- **Base URL:** `https://apiprod.fattlabs.com`
- **Official documentation:** [Void or Refund Transaction](https://docs.staxpayments.com/reference/void-or-refund-transaction)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | no | Transaction identifier |
| `total` | body | `string` | no | Refund total |

# Identify Brand from Transaction Data with Brand.dev

Identifies a brand from transaction data in Brand.dev.

## Endpoint

- **Method:** `GET`
- **Path:** `/brand/transaction_identifier`
- **Base URL:** `https://api.brand.dev/v1`
- **Official documentation:** [Identify Brand from Transaction Data](https://docs.context.dev/api-reference/retrieve-brand/identify-brand-from-transaction-data)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `transaction_info` | query | `string` | yes | Transaction data string to identify a brand from. |

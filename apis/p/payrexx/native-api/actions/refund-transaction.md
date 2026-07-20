# Refund Transaction with Payrexx

Refunds a transaction in Payrexx.

## Endpoint

- **Method:** `POST`
- **Path:** `Transaction/:id/refund`
- **Base URL:** `https://api.payrexx.com/v1.14/`
- **Official documentation:** [Refund Transaction](https://developers.payrexx.com/reference/refund-a-transaction)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | ID of the transaction to refund. |
| `amount` | body | `number` | no | Amount for refund in cents. |

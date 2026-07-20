# Cancel Invoice Transaction with Reepay

Cancels an invoice transaction in Reepay.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/invoice/:id/transaction/:transaction/cancel`
- **Base URL:** `https://api.frisbii.com`
- **Official documentation:** [Cancel Invoice Transaction](https://docs.frisbii.com/reference/canceltransaction)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Invoice id or handle from Reepay. |
| `transaction` | path | `string` | yes | Transaction id from Reepay. |

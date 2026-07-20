# Refund a transaction with Nexiopay

## Endpoint

- **Method:** `POST`
- **Path:** `/pay/v3/refund`
- **Base URL:** `https://api.nexiopaysandbox.com`
- **Official documentation:** [Refund a transaction](https://docs.nexiopay.com/reference/refundtransaction)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | yes | Nexio payment ID to refund. |
| `data` | body | `object` | yes | Refund transaction data object documented by Nexio. |

# Update Transaction Status with Dripcel

Updates a buyer transaction status in Dripcel Exchange.

## Endpoint

- **Method:** `PUT`
- **Path:** `/exchange/buyer/transaction/:id/status`
- **Base URL:** `https://api.dripcel.com`
- **Official documentation:** [Update Transaction Status](https://docs.dripcel.com/API/exchange-transactions#update-transaction-status)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | — |
| `status` | body | `string` | yes | The transaction status to apply. |

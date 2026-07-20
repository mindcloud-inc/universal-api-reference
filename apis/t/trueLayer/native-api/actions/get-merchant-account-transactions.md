# Get Merchant Account Transactions with TrueLayer

Retrieves merchant account transactions from TrueLayer.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/merchant-accounts/:id/transactions`
- **Base URL:** `https://api.truelayer-sandbox.com`
- **Official documentation:** [Get Merchant Account Transactions](https://docs.truelayer.com/docs/get-your-merchant-account-transactions-or-payment-sources)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | TrueLayer merchant account ID. |

# List Address Transactions with Mempool

Retrieves transaction history for an address from Mempool.

## Endpoint

- **Method:** `GET`
- **Path:** `/address/[:address]/txs`
- **Base URL:** `https://mempool.space/api`
- **Official documentation:** [List Address Transactions](https://mempool.space/docs/api/rest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `address` | path | `string` | yes | Bitcoin address to inspect. |

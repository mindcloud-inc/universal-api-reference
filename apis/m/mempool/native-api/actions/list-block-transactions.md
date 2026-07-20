# List Block Transactions with Mempool

Retrieves transactions from a block in Mempool.

## Endpoint

- **Method:** `GET`
- **Path:** `/block/[:hash]/txs/[:start_index]`
- **Base URL:** `https://mempool.space/api`
- **Official documentation:** [List Block Transactions](https://mempool.space/docs/api/rest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `hash` | path | `string` | yes | Block hash to inspect. |
| `start_index` | path | `number` | yes | Zero-based transaction index to start from within the block. |

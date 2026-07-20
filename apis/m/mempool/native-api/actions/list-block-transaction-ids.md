# List Block Transaction IDs with Mempool

Retrieves all transaction IDs for a block from Mempool.

## Endpoint

- **Method:** `GET`
- **Path:** `/block/[:hash]/txids`
- **Base URL:** `https://mempool.space/api`
- **Official documentation:** [List Block Transaction IDs](https://mempool.space/docs/api/rest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `hash` | path | `string` | yes | Block hash to inspect. |

# Get Block Transaction ID at Index with Mempool

Retrieves a block transaction ID from Mempool by index.

## Endpoint

- **Method:** `GET`
- **Path:** `/block/[:hash]/txid/[:index]`
- **Base URL:** `https://mempool.space/api`
- **Official documentation:** [Get Block Transaction ID at Index](https://mempool.space/docs/api/rest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `hash` | path | `string` | yes | Block hash to inspect. |
| `index` | path | `number` | yes | Zero-based transaction index within the block. |

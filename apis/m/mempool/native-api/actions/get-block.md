# Get Block with Mempool

Retrieves details about a block from Mempool.

## Endpoint

- **Method:** `GET`
- **Path:** `/block/[:hash]`
- **Base URL:** `https://mempool.space/api`
- **Official documentation:** [Get Block](https://mempool.space/docs/api/rest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `hash` | path | `string` | yes | Block hash to inspect. |

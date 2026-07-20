# Get Block Header with Mempool

Retrieves a block header from Mempool.

## Endpoint

- **Method:** `GET`
- **Path:** `/block/[:hash]/header`
- **Base URL:** `https://mempool.space/api`
- **Official documentation:** [Get Block Header](https://mempool.space/docs/api/rest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `hash` | path | `string` | yes | Block hash to inspect. |

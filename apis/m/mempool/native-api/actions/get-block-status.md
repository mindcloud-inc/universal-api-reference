# Get Block Status with Mempool

Retrieves the confirmation status of a block from Mempool.

## Endpoint

- **Method:** `GET`
- **Path:** `/block/[:hash]/status`
- **Base URL:** `https://mempool.space/api`
- **Official documentation:** [Get Block Status](https://mempool.space/docs/api/rest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `hash` | path | `string` | yes | Block hash to inspect. |

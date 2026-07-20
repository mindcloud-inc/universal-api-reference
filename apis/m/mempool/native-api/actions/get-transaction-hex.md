# Get Transaction Hex with Mempool

Retrieves a transaction serialized as hex from Mempool.

## Endpoint

- **Method:** `GET`
- **Path:** `/tx/[:txid]/hex`
- **Base URL:** `https://mempool.space/api`
- **Official documentation:** [Get Transaction Hex](https://mempool.space/docs/api/rest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `txid` | path | `string` | yes | Bitcoin transaction ID to inspect. |

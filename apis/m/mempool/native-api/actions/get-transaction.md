# Get Transaction with Mempool

Retrieves full transaction details from Mempool.

## Endpoint

- **Method:** `GET`
- **Path:** `/tx/[:txid]`
- **Base URL:** `https://mempool.space/api`
- **Official documentation:** [Get Transaction](https://mempool.space/docs/api/rest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `txid` | path | `string` | yes | Bitcoin transaction ID to inspect. |

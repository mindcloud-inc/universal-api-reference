# Get Transaction Status with Mempool

Retrieves transaction confirmation status from Mempool.

## Endpoint

- **Method:** `GET`
- **Path:** `/tx/[:txid]/status`
- **Base URL:** `https://mempool.space/api`
- **Official documentation:** [Get Transaction Status](https://mempool.space/docs/api/rest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `txid` | path | `string` | yes | Bitcoin transaction ID to inspect. |

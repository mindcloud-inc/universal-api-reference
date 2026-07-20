# Get Mining Pool with Mempool

Retrieves mining pool details from Mempool.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/mining/pool/[:slug]`
- **Base URL:** `https://mempool.space/api`
- **Official documentation:** [Get Mining Pool](https://mempool.space/docs/api/rest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `slug` | path | `string` | yes | Mempool mining pool slug, such as foundryusa. |

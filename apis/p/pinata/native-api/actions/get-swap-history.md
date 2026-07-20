# Get Swap History with Pinata

Retrieves CID swap history from Pinata.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/files/:network/swap/:cid`
- **Base URL:** `https://api.pinata.cloud`
- **Official documentation:** [Get Swap History](https://docs.pinata.cloud/api-reference/endpoint/get-swap-history)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cid` | path | `string` | yes | Original CID to inspect. |
| `domain` | query | `string` | yes | Gateway domain with the Hot Swaps plugin installed. |
| `network` | path | `string` | yes | Target network (`public` or `private`). |

# Add Swap with Pinata

Updates a CID swap mapping in Pinata.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v3/files/:network/swap/:cid`
- **Base URL:** `https://api.pinata.cloud`
- **Official documentation:** [Add Swap](https://docs.pinata.cloud/api-reference/endpoint/add-swap)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cid` | path | `string` | yes | Original CID to swap. |
| `network` | path | `string` | yes | Target network (`public` or `private`). |
| `swapCid` | body | `string` | yes | CID to redirect to. |

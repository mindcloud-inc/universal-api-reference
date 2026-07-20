# Remove Swap with Pinata

Deletes an existing CID swap from Pinata.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v3/files/:network/swap/:cid`
- **Base URL:** `https://api.pinata.cloud`
- **Official documentation:** [Remove Swap](https://docs.pinata.cloud/api-reference/endpoint/remove-swap)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cid` | path | `string` | yes | Original CID whose swap should be removed. |
| `network` | path | `string` | yes | Target network (`public` or `private`). |

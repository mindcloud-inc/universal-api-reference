# Pin JSON with Pinata

Creates a new pinned JSON object in Pinata.

## Endpoint

- **Method:** `POST`
- **Path:** `/pinning/pinJSONToIPFS`
- **Base URL:** `https://api.pinata.cloud`
- **Official documentation:** [Pin JSON](https://docs.pinata.cloud/api-reference/endpoint/ipfs/pin-json-to-ipfs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pinataContent` | body | `object` | yes | JSON object to pin to IPFS. |

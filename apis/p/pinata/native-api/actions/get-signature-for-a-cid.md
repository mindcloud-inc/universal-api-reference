# Get Signature for a CID with Pinata

Retrieves a CID signature from Pinata.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/files/:network/signature/:cid`
- **Base URL:** `https://api.pinata.cloud`
- **Official documentation:** [Get Signature for a CID](https://docs.pinata.cloud/api-reference/endpoint/get-signature-for-a-cid)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cid` | path | `string` | yes | Target CID. |
| `network` | path | `string` | yes | Target network (`public` or `private`). |

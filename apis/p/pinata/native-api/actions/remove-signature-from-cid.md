# Remove Signature from CID with Pinata

Deletes an existing CID signature from Pinata.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v3/files/:network/signature/:cid`
- **Base URL:** `https://api.pinata.cloud`
- **Official documentation:** [Remove Signature from CID](https://docs.pinata.cloud/api-reference/endpoint/remove-signature-from-cid)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cid` | path | `string` | yes | Target CID. |
| `network` | path | `string` | yes | Target network (`public` or `private`). |

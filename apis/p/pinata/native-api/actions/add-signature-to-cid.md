# Add Signature to CID with Pinata

Creates a new CID signature in Pinata.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/files/:network/signature/:cid`
- **Base URL:** `https://api.pinata.cloud`
- **Official documentation:** [Add Signature to CID](https://docs.pinata.cloud/api-reference/endpoint/add-signature-to-cid)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `address` | body | `string` | yes | Wallet address that created the signature. |
| `cid` | path | `string` | yes | Target CID. |
| `network` | path | `string` | yes | Target network (`public` or `private`). |
| `signature` | body | `string` | yes | Signature for the target CID. |

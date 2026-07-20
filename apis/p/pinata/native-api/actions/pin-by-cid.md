# Pin by CID with Pinata

Creates a new pin request in Pinata by CID.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/files/public/pin_by_cid`
- **Base URL:** `https://api.pinata.cloud`
- **Official documentation:** [Pin by CID](https://docs.pinata.cloud/api-reference/endpoint/pin-by-cid)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cid` | body | `string` | yes | CID to pin. |

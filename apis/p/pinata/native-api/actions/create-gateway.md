# Create Gateway with Pinata

Creates a new gateway in Pinata.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/gateways`
- **Base URL:** `https://api.pinata.cloud`
- **Official documentation:** [Create Gateway](https://docs.pinata.cloud/api-reference/endpoint/ipfs/create-gateway)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain` | body | `string` | yes | Desired gateway subdomain name. |

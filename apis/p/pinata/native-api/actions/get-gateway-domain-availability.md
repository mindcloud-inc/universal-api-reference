# Get Gateway Domain Availability with Pinata

Retrieves gateway domain availability from Pinata.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/gateways/exists/:domain`
- **Base URL:** `https://api.pinata.cloud`
- **Official documentation:** [Get Gateway Domain Availability](https://docs.pinata.cloud/api-reference/endpoint/ipfs/gateway-domain-available)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain` | path | `string` | yes | Gateway subdomain to check. |

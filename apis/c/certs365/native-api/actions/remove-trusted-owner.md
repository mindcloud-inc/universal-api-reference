# Remove Trusted Owner with Certs 365

Removes a trusted owner role in Certs 365.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/remove-trusted-owner`
- **Base URL:** `https://api1.certs365.io`
- **Official documentation:** [Remove Trusted Owner](https://help.certs365.io/documentation/blockchain/remove-trusted-owner-revoke-role/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `address` | body | `string` | yes | Ethereum address to which the role will be revoked. |

# Add Trusted Owner with Certs 365

Adds a trusted owner role in Certs 365.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/add-trusted-owner`
- **Base URL:** `https://api1.certs365.io`
- **Official documentation:** [Add Trusted Owner](https://help.certs365.io/documentation/blockchain/add-trusted-owner-grant-role/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `address` | body | `string` | yes | Ethereum address to which the role will be assigned. |

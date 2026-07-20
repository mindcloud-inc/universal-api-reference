# Create And Validate Issuer with Certs 365

Creates and validates an issuer in Certs 365.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/create-validate-issuer`
- **Base URL:** `https://api1.certs365.io`
- **Official documentation:** [Create And Validate Issuer](https://help.certs365.io/documentation/blockchain/create-validate-issuer-internal/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Email of the issuer to create and approve. |

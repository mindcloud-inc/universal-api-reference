# Validate Issuer with Certs 365

Validates an issuer in Certs 365.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/validate-issuer`
- **Base URL:** `https://api1.certs365.io`
- **Official documentation:** [Validate Issuer](https://help.certs365.io/documentation/blockchain/validate-issuer/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `status` | body | `number` | yes | Status code indicating approval (1) or rejection (2). |
| `email` | body | `string` | yes | Email of the issuer to be approved or rejected. |

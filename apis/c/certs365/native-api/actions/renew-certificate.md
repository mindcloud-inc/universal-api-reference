# Renew Certificate with Certs 365

Updates a certificate expiration in Certs 365.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/renew-cert`
- **Base URL:** `https://api1.certs365.io`
- **Official documentation:** [Renew Certificate](https://help.certs365.io/documentation/code-module-apis/renew-certification-extend-expiration-single/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Issuer email. |
| `certificateNumber` | body | `string` | yes | Certificate number. |
| `expirationDate` | body | `date` | yes | New certificate expiration date. |

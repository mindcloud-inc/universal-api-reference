# Update Certificate Status with Certs 365

Updates a certificate status in Certs 365.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/update-cert-status`
- **Base URL:** `https://api1.certs365.io`
- **Official documentation:** [Update Certificate Status](https://help.certs365.io/documentation/code-module-apis/revoke-reactivate-certification-single/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Issuer email. |
| `certificateNumber` | body | `string` | yes | Certificate number. |
| `certStatus` | body | `number` | yes | Certificate status value. |

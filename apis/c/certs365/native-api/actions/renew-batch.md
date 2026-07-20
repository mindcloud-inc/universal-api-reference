# Renew Batch with Certs 365

Updates batch certificate expirations in Certs 365.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/renew-batch`
- **Base URL:** `https://api1.certs365.io`
- **Official documentation:** [Renew Batch](https://help.certs365.io/documentation/code-module-apis/renew-certification-extend-expiration-batch/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Issuer email. |
| `batch` | body | `number` | yes | Certificate batch number. |
| `expirationDate` | body | `date` | yes | New batch expiration date. |

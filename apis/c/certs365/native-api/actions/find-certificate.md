# Find Certificate with Certs 365

Finds a certificate in Certs 365 by ID or name.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/get-issue`
- **Base URL:** `https://api1.certs365.io`
- **Official documentation:** [Find Certificate](https://help.certs365.io/documentation/fetching-upload-request-details/get-a-specific-certificate-on-id-or-name-based-search/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Issuer email address. |
| `input` | body | `string` | yes | Certificate ID or name to search for. |
| `type` | body | `number` | yes | Search type: 1 for renew, 2 for reactivate, 3 for revoke. |

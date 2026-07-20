# Get Single Certificates with Certs 365

Retrieves single certificates from Certs 365 storage.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/get-single-certificates`
- **Base URL:** `https://api1.certs365.io`
- **Official documentation:** [Get Single Certificates](https://help.certs365.io/documentation/fetching-upload-request-details/get-single-with-without-pdf-certifications-from-s3/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `issuerId` | body | `string` | yes | Issuer ID. |
| `type` | body | `number` | yes | Certificate type: 1 with PDF, 2 without PDF. |

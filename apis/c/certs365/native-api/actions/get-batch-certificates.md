# Get Batch Certificates with Certs 365

Retrieves batch certificates from Certs 365 storage.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/get-batch-certificates`
- **Base URL:** `https://api1.certs365.io`
- **Official documentation:** [Get Batch Certificates](https://help.certs365.io/documentation/fetching-upload-request-details/get-batch-certifications-from-s3/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `issuerId` | body | `string` | yes | Issuer ID. |
| `batchId` | body | `string` | yes | Batch ID. |

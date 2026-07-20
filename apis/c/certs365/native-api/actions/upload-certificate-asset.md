# Upload Certificate Asset with Certs 365

Uploads a certificate asset to Certs 365 storage.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/upload-certificate`
- **Base URL:** `https://api1.certs365.io`
- **Official documentation:** [Upload Certificate Asset](https://help.certs365.io/documentation/fetching-upload-request-details/upload-certification-into-aws-s3/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `file` | yes | Certificate file to upload. |
| `certificateNumber` | body | `string` | yes | The ID or number of the certificate. |
| `type` | body | `number` | yes | Certificate type: 1 with PDF, 2 without PDF, 3 batch. |

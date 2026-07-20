# Upload Media File with Certs 365

Uploads a media file to Certs 365 storage.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/upload`
- **Base URL:** `https://api1.certs365.io`
- **Official documentation:** [Upload Media File](https://help.certs365.io/documentation/fetching-upload-request-details/upload-media-file-into-s3/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `file` | yes | Media file to upload to S3. |

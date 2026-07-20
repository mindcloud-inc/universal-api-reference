# Get PDF XMP Metadata with DynamicPDF

Retrieves PDF XMP metadata from DynamicPDF API.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1.0/pdf-xmp`
- **Base URL:** `https://api.dpdf.io`
- **Official documentation:** [Get PDF XMP Metadata](https://dpdf.io/docs/usersguide/cloud-api/cloud-api-pdf-xmp)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/pdf` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `PDF` | body | `file` | yes | PDF file sent as the raw request body. |

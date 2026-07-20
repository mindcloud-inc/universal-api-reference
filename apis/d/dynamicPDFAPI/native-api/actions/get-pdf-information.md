# Get PDF Information with DynamicPDF

Retrieves information about a PDF from DynamicPDF API.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1.0/pdf-info`
- **Base URL:** `https://api.dpdf.io`
- **Official documentation:** [Get PDF Information](https://dpdf.io/docs/usersguide/cloud-api/cloud-api-pdf-info)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/pdf` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `PDF` | body | `file` | yes | PDF file sent as the raw request body. |

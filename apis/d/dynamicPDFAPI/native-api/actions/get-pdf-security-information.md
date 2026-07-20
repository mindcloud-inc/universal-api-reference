# Get PDF Security Information with DynamicPDF

Retrieves PDF security information from DynamicPDF API.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1.0/pdf-security-info`
- **Base URL:** `https://api.dpdf.io`
- **Official documentation:** [Get PDF Security Information](https://dpdf.io/docs/usersguide/cloud-api/cloud-api-pdf-security-info)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/pdf` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `PDF` | body | `file` | yes | PDF file sent as the raw request body. |

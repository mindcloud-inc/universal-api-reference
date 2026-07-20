# Convert HTML To PDF with DynamicPDF

Converts HTML to a PDF in DynamicPDF API.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1.0/pdf`
- **Base URL:** `https://api.dpdf.io`
- **Official documentation:** [Convert HTML To PDF](https://dpdf.io/docs/convert-html-to-pdf)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Instructions` | body | `file` | yes | DynamicPDF instructions JSON uploaded as the Instructions multipart part. |
| `Resource` | body | `file` | yes | HTML file content uploaded to DynamicPDF as a Resource part. |
